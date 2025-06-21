# Personal File and Text Management System

A comprehensive Node.js-based server application that functions as a personal file and text management system, accessible from any location with an internet connection.

## Features

### File Management
- **Upload Files**: Support for various file types including documents, images, and text files
- **File Storage**: Local storage on the deployment environment
- **File Operations**: View, download, delete, and share files
- **Drag & Drop**: Easy file upload with drag and drop interface
- **File Sharing**: Generate shareable links for files

### Built-in Notepad
- **Create Notes**: Built-in text editor for creating notes
- **Edit Notes**: Modify existing notes with real-time editing
- **Persistent Storage**: Notes are saved until explicitly deleted
- **Note Management**: List, select, and organize notes

### Security
- **Authentication**: Secure login system with predefined admin credentials
- **Session Management**: Secure session handling
- **Access Control**: Protected routes requiring authentication

### User Interface
- **Responsive Design**: Works on desktop and mobile devices
- **Modern UI**: Clean and intuitive interface
- **Tab-based Navigation**: Easy switching between file manager and notepad

## Installation

1. **Clone or download the project files**

2. **Install dependencies**:
   \`\`\`bash
   npm install
   \`\`\`

3. **Start the server**:
   \`\`\`bash
   npm start
   \`\`\`
   
   For development with auto-restart:
   \`\`\`bash
   npm run dev
   \`\`\`

4. **Access the application**:
   Open your browser and go to `http://localhost:3000`

## Default Credentials

s

## API Endpoints

### Authentication
- `POST /api/login` - User login
- `POST /api/logout` - User logout
- `GET /api/auth-status` - Check authentication status

### File Management
- `POST /api/upload` - Upload files
- `GET /api/files` - Get all files
- `GET /api/download/:filename` - Download file
- `DELETE /api/files/:filename` - Delete file
- `POST /api/share/:filename` - Generate share link
- `GET /shared/:shareId` - Access shared file

### Notes Management
- `GET /api/notes` - Get all notes
- `POST /api/notes` - Create or update note
- `GET /api/notes/:id` - Get specific note
- `DELETE /api/notes/:id` - Delete note

## File Structure

\`\`\`
project/
├── server.js              # Main server file
├── package.json           # Dependencies and scripts
├── public/
│   ├── login.html         # Login page
│   └── dashboard.html     # Main dashboard
├── uploads/               # Uploaded files storage
├── notes/                 # Notes storage
└── README.md             # This file
\`\`\`

## Configuration

### Environment Variables
You can set the following environment variables:

- `PORT` - Server port (default: 3000)

### Security Notes
- Change the session secret in production
- Use HTTPS in production
- Consider implementing rate limiting
- Regular backup of uploads and notes directories

## Usage

### File Management
1. Login with the provided credentials
2. Navigate to the "File Manager" tab
3. Upload files by dragging and dropping or clicking "Select Files"
4. Manage files using download, share, or delete options

### Notepad
1. Navigate to the "Notepad" tab
2. Click "New Note" to create a new note
3. Enter a title and content
4. Click "Save Note" to persist the note
5. Select existing notes from the list to edit

### File Sharing
1. Click the "Share" button on any file
2. Copy the generated share link
3. Share the link with others for file access

## Technical Details

- **Backend**: Node.js with Express.js
- **File Upload**: Multer middleware
- **Session Management**: express-session
- **File Storage**: Local filesystem
- **Frontend**: Vanilla HTML, CSS, and JavaScript

## Deployment

The application can be deployed on any Node.js hosting platform:

1. **Heroku**: Push to Heroku with the included package.json
2. **VPS**: Run on any VPS with Node.js installed
3. **Cloud Platforms**: Deploy on AWS, Google Cloud, or Azure

Make sure to:
- Set appropriate environment variables
- Configure file storage permissions
- Use HTTPS in production
- Set up regular backups

## License

MIT License - Feel free to modify and use as needed.
