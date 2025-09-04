# LASU E-Voting System

A comprehensive student voting platform with secure authentication, document verification, and biometric face recognition.

## Features

### Student Registration & Verification
- Google OAuth 2.0 authentication
- Course form document upload (PDF only, max 10MB)
- Automatic document verification against student details
- SkyBiometry face recognition for liveness check
- One face per account security

### Voting System
- Secure voting platform for activated accounts only
- View candidates and positions
- Cast votes with full audit trail

### Admin Panel
- Upload candidates and manage positions
- Start/end voting periods
- Real-time vote counting and results

## Tech Stack

### Frontend
- Next.js 14 with TypeScript
- Tailwind CSS for styling
- Google OAuth 2.0 integration

### Backend
- C# .NET 8 Web API
- PostgreSQL database (hosted on Render)
- Cloudinary for PDF storage
- SkyBiometry API for face recognition

## Getting Started

### Prerequisites
- Node.js 18+
- .NET 8 SDK
- PostgreSQL access

### Environment Variables

#### Frontend (.env.local)
```
NEXT_PUBLIC_GOOGLE_CLIENT_ID=********************************************
NEXT_PUBLIC_API_URL=***********
```

#### Backend (appsettings.json)
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "*****************************"
  },
  "GoogleAuth": {
    "ClientId": "***************************",
    "ClientSecret": "***************************"
  },
  "Cloudinary": {
    "CloudName": "*******",
    "ApiKey": "**************",
    "ApiSecret": "**************"
  },
  "SkyBiometry": {
    "ApiKey": "*******************",
    "ApiSecret": "***************",
    "Namespace": "****************"
  }
}
```

### Installation

1. Clone the repository
2. Install frontend dependencies:
   ```bash
   cd frontend
   npm install
   ```
3. Install backend dependencies:
   ```bash
   cd backend
   dotnet restore
   ```
4. Run the applications:
   ```bash
   # Frontend
   cd frontend && npm run dev
   
   # Backend
   cd backend && dotnet run
   ```

## Project Structure

```
├── frontend/          # Next.js frontend application
├── backend/           # .NET 8 Web API
└── README.md
```
