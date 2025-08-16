# 🗳️ Romanian Online Voting System

**A comprehensive online voting platform designed for Romanian national elections, built with ASP.NET Core 8.0 and Entity Framework Core.**

## 🎯 **Primary Goal: Online Voting for Romanian Elections**

This system is specifically designed to **enable secure, transparent, and accessible online voting** for Romanian citizens during national elections. The platform manages political parties, candidates, and provides the foundation for implementing secure digital voting mechanisms.

## 🏛️ **What This System Does**

**Core Purpose**: Create a digital infrastructure for Romanian citizens to vote online in elections, replacing or supplementing traditional paper-based voting.

**Key Features**:
- **Political Party Management**: Full CRUD operations for Romanian political parties
- **Candidate Management**: Complete candidate lifecycle management with party associations  
- **Voting Infrastructure**: Foundation for implementing secure online voting mechanisms
- **Statistics Dashboard**: Real-time analytics for election monitoring
- **Automated Testing**: Background service for generating sample election data

## 🏗️ **Technology Stack**

- **Backend**: ASP.NET Core 8.0 MVC
- **Database**: SQL Server with Entity Framework Core 8.0.6
- **Frontend**: Razor Views with Bootstrap
- **Containerization**: Docker support
- **Deployment**: Heroku-ready

## 🚀 **Quick Start**

### Prerequisites
- .NET 8.0 SDK
- SQL Server (LocalDB recommended)
- Visual Studio 2022 or VS Code

### Installation
```bash
git clone <repository-url>
cd MPP-SMTH
dotnet restore
dotnet ef database update
dotnet run
```

Access at `https://localhost:5001`

## 📊 **Data Models**

### Party Model
- **PartyId**: Unique identifier
- **Name**: Party name (PSD, PNL, USR, AUR, etc.)
- **Description**: Party description
- **LogoUrl**: Party logo
- **Candidates**: Associated candidates

### Candidate Model  
- **CandidateId**: Unique identifier
- **Name**: Candidate full name
- **Description**: Candidate description
- **ImageUrl**: Candidate photo
- **Age**: Candidate age (18-120)
- **Position**: Political position (Deputat, Senator, etc.)
- **PartyId**: Associated party

## 🔧 **How to Use**

### Managing Elections
1. **Parties**: Navigate to `/Party` to manage political parties
2. **Candidates**: Go to `/Candidate` to manage election candidates
3. **Statistics**: Visit `/Statistics` for election overview
4. **Auto-Generation**: Use automated tools to populate sample election data

### Romanian Election Context
The system comes pre-loaded with major Romanian political parties:
- **PSD** (Partidul Social Democrat)
- **PNL** (Partidul Național Liberal) 
- **USR** (Uniunea Salvați România)
- **AUR** (Alianța pentru Unirea Românilor)

## 🗳️ **Voting System Foundation**

**This application serves as the foundation for implementing:**
- **Secure Online Voting**: Digital ballot casting for Romanian citizens
- **Voter Authentication**: Secure identity verification systems
- **Real-time Results**: Live election result tracking
- **Audit Trails**: Complete voting record maintenance
- **Accessibility**: Voting from anywhere with internet access

## 🐳 **Docker Support**

```bash
docker build -t romanian-voting-system .
docker run -p 8080:80 romanian-voting-system
```

## 🚀 **Deployment**

### Heroku
- Includes Procfile for easy Heroku deployment
- Configure database connection string
- Run migrations

### Azure
- Publish to Azure App Service
- Configure SQL Database connection
- Deploy with Azure DevOps

## 🔒 **Security Features**

- **Anti-forgery Tokens**: CSRF protection
- **Input Validation**: Comprehensive data validation
- **SQL Injection Protection**: Entity Framework Core
- **Authorization Framework**: Built-in ASP.NET Core security

## 📝 **API Endpoints**

- **Parties**: `/Party` - Full CRUD operations
- **Candidates**: `/Candidate` - Complete candidate management  
- **Statistics**: `/Statistics` - Election analytics
- **Auto-generation**: `/Candidate/StartGenerating` - Sample data creation

## 🐛 **Troubleshooting**

- **Database Issues**: Check LocalDB is running, verify connection string
- **Migration Errors**: Drop and recreate database with `dotnet ef database drop`
- **Port Conflicts**: Modify `launchSettings.json` if needed

---

## 🎯 **Important Note**

**This system is specifically designed to enable online voting for Romanian national elections.** It provides the complete infrastructure needed to conduct secure, transparent, and accessible digital voting, allowing Romanian citizens to participate in democracy from anywhere in the world.

**When implementing actual voting functionality, ensure compliance with:**
- Romanian electoral laws and regulations
- European Union data protection standards (GDPR)
- International election security best practices
- Local data sovereignty requirements

**Current Status**: Foundation complete - ready for voting mechanism implementation.
