## Project #2 - Music Discovery App

A modern, interactive front-end web application inspired by Spotify that provides users with an engaging music exploration and playback experience. The app features a unique circular queue visualization, dynamic color schemes that adapt to album art, and seamless integration with the Spotify Web API for real-time playback control and music discovery.

**Contributors**: Damien Hall, Juan Figueroa, Briana Daniels

- **What are the users?**  
  Music enthusiasts and Spotify users who want an alternative, visually engaging interface for discovering music, controlling playback, and exploring their listening queue in an innovative way.

- **What job does it form for them?**  
  The Music Discovery App serves as an interactive music player and exploration tool that allows users to authenticate with Spotify, search for tracks and artists, view and manage playlists, control playback (play, pause, skip, seek), and visualize their upcoming queue in a unique circular layout. It provides a personalized experience through dynamic UI color schemes that adapt to album artwork.

- **What inspired you to make it?**  
  The inspiration came from reimagining the traditional music player interface. By creating a circular queue visualization and album art-driven color schemes, we aimed to make music exploration more visually engaging and intuitive. The project provided an opportunity to work with modern React patterns, TypeScript, and external API integration while creating a polished user experience.

- **What features are the most important?**
  - **Spotify OAuth2 Authentication**: Secure login using PKCE (Proof Key for Code Exchange) flow with token management
  - **Circular Queue Ring**: Innovative circular visualization displaying upcoming tracks in the playback queue
  - **Dynamic Color Scheme**: UI automatically adapts to album artwork colors using Chroma.js for personalized aesthetics
  - **Now Playing View**: Real-time display of current track information, album art, and playback controls
  - **Interactive Player Controls**: Complete playback functionality including play, pause, skip, and seek operations
  - **Music Search**: Real-time search for tracks and artists using Spotify's Search API
  - **Context-Based State Management**: Global state handling through React Context API for authentication, playback, colors, and playlists
  - **Responsive Design**: Scales beautifully across devices and screen sizes with Material UI components

- **Include relevant screenshots**  
  _(Add screenshots of the circular queue ring, now playing view, music search interface, and dynamic color scheme examples)_

## Technologies

### Languages
- TypeScript (primary language for type safety)
- JavaScript (ES6+)
- CSS (styling and animations)

### Frontend Framework & Build Tools
- React 19 (component-based UI framework)
- Vite (modern build tool and development server)

### UI Libraries & Styling
- Material UI (MUI) (component library)
- Chroma.js (color manipulation and palette generation)
- Responsive design patterns

### Utilities & Helpers
- Lodash (utility functions)
- Custom hooks for API calls and state logic

### External API Integration
- Spotify Web API (authentication, playback control, search, user data)
- OAuth2 PKCE flow implementation

### State Management
- React Context API (global state)
- Custom Context Providers:
  - SpotifyAPIContext (API calls and auth)
  - PlayerContext (playback state and queue)
  - ColorSchemeContext (dynamic UI colors)
  - PlaylistContext (playlist management)
  - SearchContext (search state)

### Development Tools
- Node.js (v18+)
- npm (package management)

## Competencies

### JF 1.5: Can work effectively and contribute appropriately on a team to produce software
- **Situation**: As part of a three-person development team, we needed to build a complex music application with multiple interconnected features including authentication, playback control, search functionality, and innovative UI components like the circular queue ring.
- **Actions**: I collaborated with Damien Hall and Juan Figueroa to divide responsibilities across component development, API integration, and UI/UX features. We established a component-based architecture with clear separation of concerns, created shared Context providers for global state management, implemented reusable components (MusicPlayer, PlayBar, QueueRing, Playlist), and used version control for collaborative development. We maintained consistent coding standards with TypeScript for type safety across the codebase.
- **Results**: Successfully delivered a fully functional music discovery app with seamless integration between all components. Our collaborative approach enabled parallel development where team members could work on different features (player controls, search, queue visualization) while sharing state through Context providers. The modular architecture allowed easy integration and testing of individual components.
- **Connection**: This project demonstrates effective team software development through clear architectural planning, shared state management patterns, reusable component design, collaborative problem-solving for Spotify API integration, and consistent use of TypeScript for team-wide type safety.

### JF 2.3: Can develop effective user interfaces
- **Situation**: The music player needed to stand out with innovative UI features while maintaining usability, including a unique circular queue visualization, album art integration, and dynamic color schemes that adapt to the currently playing track.
- **Actions**: I designed and implemented an interactive circular queue ring that visually displays upcoming tracks in a unique layout, created a dynamic color scheme system using Chroma.js that extracts colors from album artwork and applies them across the UI, built responsive layouts using Material UI components that scale across devices, implemented smooth animations and transitions for playback controls, and designed an intuitive music search interface with real-time results. The UI adapts to album art colors for a personalized, immersive experience.
- **Results**: The application features a visually stunning and highly interactive interface that differentiates it from traditional music players. The circular queue ring provides an innovative way to visualize upcoming tracks, and the dynamic color scheme creates a personalized experience for each song. User feedback highlights the engaging visual design and intuitive controls. The responsive design ensures functionality across desktop, tablet, and mobile devices.
- **Connection**: This project showcases advanced UI/UX design skills through innovative visualization techniques (circular queue), dynamic theming based on content, responsive design implementation with Material UI, smooth user interactions, and creation of an aesthetically pleasing interface that enhances user engagement.

### JF 3.8: Can encrypt sensitive data via hashing and strive to implement OWASP recommended security practices
- **Situation**: The application requires Spotify authentication, which involves handling OAuth2 tokens, managing user sessions, and ensuring secure communication with the Spotify API while protecting sensitive user credentials and access tokens.
- **Actions**: I implemented OAuth2 PKCE (Proof Key for Code Exchange) flow for secure authentication without exposing client secrets, designed secure token storage and management in the SpotifyAPIContext, ensured all API calls use HTTPS connections to Spotify's endpoints, implemented proper token refresh logic to maintain sessions securely, and followed OAuth2 best practices for redirect URIs and state management. The PKCE flow provides additional security for public clients like single-page applications.
- **Results**: Successfully implemented secure Spotify authentication that protects user credentials and access tokens. The PKCE flow ensures that authorization codes cannot be intercepted and used by malicious actors. Tokens are managed securely in memory through the Context API, and all communications with Spotify use encrypted HTTPS connections. Users can authenticate safely and maintain secure sessions throughout their app usage.
- **Connection**: This project demonstrates security awareness through implementation of OAuth2 PKCE for secure authentication, proper token management practices, encrypted API communications, and adherence to OAuth2 security best practices for protecting user credentials in a client-side application.

### JF 4.4: Can interpret and implement a given design while remaining compliant with security and maintainability requirements
- **Situation**: The project required building a Spotify-inspired music player with specific features (authentication, search, playback controls, queue visualization) while maintaining clean architecture, type safety, and integration with external APIs under the constraints of a front-end application.
- **Actions**: I architected the application using React 19 with TypeScript for type safety and maintainability, implemented a component-based structure with clear separation of concerns (UI components, Context providers, API handlers, utility functions), created five Context providers for global state management (API, Player, ColorScheme, Playlist, Search), integrated Spotify Web API following their documentation and best practices, and established consistent patterns for API calls, error handling, and state updates. The architecture supports easy extension and testing of individual components.
- **Results**: Delivered a maintainable, type-safe application with clear architectural boundaries. TypeScript provides compile-time error checking and better developer experience. The Context-based state management allows components to access global state without prop drilling. The modular design enables easy feature additions and component reuse. All Spotify API integrations follow official documentation and handle errors gracefully.
- **Connection**: This project demonstrates the ability to interpret requirements and implement maintainable solutions through TypeScript for type safety, component-based architecture with clear responsibilities, Context API for scalable state management, proper integration with external APIs, and establishment of consistent patterns that enhance code maintainability and team collaboration.