# Flowverse-Prototype-
Under Development

# FlowVerse - Indian Hip-Hop Revolution

![FlowVerse](https://images.unsplash.com/photo-1470225620780-dba8ba36b745?w=800)

FlowVerse is a revolutionary music streaming platform specifically designed for the Indian Hip-Hop community. It provides a space for artists to share their music, sell merchandise, and connect directly with their fans through a unique payment system.

## 🎵 Features

- **Music Streaming**: Seamless playback of tracks from both YouTube and local sources
- **Artist Profiles**: Dedicated spaces for artists to showcase their work
- **Merchandise Store**: Built-in e-commerce platform for artist merchandise
- **Direct Support**: UPI-based payment system for fans to support artists
- **Genre Discovery**: Browse music by different regional hip-hop styles
- **3D Visualizer**: Interactive audio visualization using Three.js
- **Real-time Search**: Search tracks across multiple platforms

## 🚀 Tech Stack

- **Frontend**: React with TypeScript
- **Styling**: Tailwind CSS
- **Database**: Supabase
- **Authentication**: Supabase Auth
- **3D Graphics**: Three.js with React Three Fiber
- **State Management**: Zustand
- **Icons**: Lucide React
- **Audio Processing**: Web Audio API
- **Video Integration**: YouTube API

## 📦 Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up environment variables in `.env`:
   ```
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_supabase_key
   VITE_YOUTUBE_API_KEY=your_youtube_api_key
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```

## 🗄️ Database Schema

### Users Table
- `id`: UUID (Primary Key)
- `username`: Text
- `avatar_url`: Text
- `is_artist`: Boolean
- `upi_id`: Text
- `created_at`: Timestamp

### Tracks Table
- `id`: UUID (Primary Key)
- `title`: Text
- `artist_id`: UUID (References users)
- `cover_url`: Text
- `audio_url`: Text
- `genre`: Text
- `created_at`: Timestamp

### Plays Table
- `id`: UUID (Primary Key)
- `track_id`: UUID (References tracks)
- `user_id`: UUID (References users)
- `played_at`: Timestamp

### Payments Table
- `id`: UUID (Primary Key)
- `from_user_id`: UUID (References users)
- `to_artist_id`: UUID (References users)
- `track_id`: UUID (References tracks)
- `amount`: Numeric
- `upi_transaction_id`: Text
- `created_at`: Timestamp

## 🔐 Security Features

- Row Level Security (RLS) enabled on all tables
- Secure authentication flow
- Protected API endpoints
- UPI transaction verification

## 🎨 UI Components

- **Home**: Featured tracks and genre browser
- **Player**: Custom audio player with YouTube integration
- **Search**: Real-time search across platforms
- **Merch Store**: E-commerce interface
- **Artist Dashboard**: Analytics and order management
- **3D Scene**: Interactive audio visualizer

## 📱 Responsive Design

The application is fully responsive and works seamlessly across:
- Desktop browsers
- Tablets
- Mobile devices

## 🔄 State Management

Using Zustand for managing:
- Current track and playback state
- User authentication
- Search results
- Shopping cart
- Audio settings

## 🎯 Future Enhancements

1. **Offline Support**
   - PWA implementation
   - Local track caching

2. **Social Features**
   - Artist following
   - User playlists
   - Track sharing

3. **Advanced Analytics**
   - Play count tracking
   - Revenue analytics
   - Audience insights

4. **Content Creation**
   - Built-in recording studio
   - Beat marketplace
   - Collaboration tools

## 📄 License

MIT License - see LICENSE file for details
