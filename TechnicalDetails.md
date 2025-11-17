# Business Central On-Premise Environment Setup for "Customer Name"
 
## Environment Details
 
### Production Environment
- **Server**: [SERVER_NAME/IP]
- **Server Instance**: BC250
- **HTTP Port**: 7149
- **SOAP Port**: 7150
- **OData Port**: 7148
- **Management Port**: 7145
- **Current Build**: [CHECK_AND_UPDATE]
- **Platform Version**: 27.0
- **Database Server**: [SQL_SERVER_NAME]
- **Database Name**: [PROD_DB_NAME]
- **Last Updated**: 2025-11-14
- **Authentication**: Windows/NavUserPassword
 
### Sandbox Environment
- **Server**: [SERVER_NAME/IP]
- **Server Instance**: BC250-SANDBOX
- **HTTP Port**: 7049
- **SOAP Port**: 7050
- **OData Port**: 7048
- **Management Port**: 7045
- **Current Build**: [CHECK_AND_UPDATE]
- **Platform Version**: 27.0
- **Database Server**: [SQL_SERVER_NAME]
- **Database Name**: [SANDBOX_DB_NAME]
- **Last Updated**: 2025-11-14
- **Authentication**: NavUserPassword
 
### Development Environment
- **Server**: localhost
- **Server Instance**: BC250-DEV
- **HTTP Port**: 7049
- **Database**: Local SQL Express/Developer
- **Last Updated**: 2025-11-14
 
## Port Configuration Matrix
 
| Environment | HTTP | HTTPS | SOAP | OData | Mgmt | Client |
|-------------|------|-------|------|-------|------|--------|
| Production  | 7149 | 7150  | 7150 | 7148  | 7145 | 7146   |
| Sandbox     | 7049 | 7050  | 7050 | 7048  | 7045 | 7046   |
| Development | 7049 | 7050  | 7050 | 7048  | 7045 | 7046   |
 
## Database Backup Strategy
 
### Production
- **Full Backup**: Daily at 2:00 AM
- **Differential**: Every 6 hours
- **Transaction Log**: Every 15 minutes
- **Retention**: 30 days full, 7 days differential
 
### Sandbox
- **Full Backup**: Daily at 3:00 AM
- **Retention**: 7 days
 
## Update Tracking
 
| Date       | Environment | From Version | To Version | Extensions Updated | Extension name &Notes |
|------------|-------------|--------------|------------|-------------------|-------|
| 14-11-2025 | -           | -            | -          | -                 | Initial Setup |
 
## Azure DevOps Repository Tracking
 
### Repository Information
- **Organization**: [WINSPIRESG]
- **Project**: [Skechers SG]
- **Repository**: [https://dev.azure.com/WinspireSG/Skechers]
- **Repository URL**: https://dev.azure.com/WinspireSG/Skechers/_git/[REPO]
 
### Branch Strategy
- **Main/Master**: Production-ready code
- **Development**: Development branch
- **Feature Branches**: feature/[feature-name]
- **Hotfix Branches**: hotfix/[issue-number]
 
### Deployment Status
 
| Date       | Environment | Branch | Commit ID | Deployed By | Azure Repo Updated | Build Pipeline | Notes |
|------------|-------------|--------|-----------|-------------|-------------------|----------------|-------|
| 14-11-2025 | -           | -      | -         | -           | ❌ Not Synced      | -              | Initial Setup |
 
**Legend:**
- ✅ Synced - Code committed and pushed to Azure Repos
- ❌ Not Synced - Local changes not yet committed
- ⚠️ Partial - Some changes committed, others pending
 
### Pre-Deployment Checklist
 
Before deploying to any environment, verify:
 
- [ ] All code changes committed to local git
- [ ] Code pushed to Azure DevOps repository
- [ ] Branch name documented in deployment tracking table
- [ ] Commit ID recorded for rollback reference
- [ ] Azure Pipeline build completed successfully (if configured)
- [ ] Code review completed (for production deployments)
- [ ] Release notes updated
 
 
## Network Configuration
 
### DNS Records
- Production: bc-prod.yourdomain.com → [PROD_SERVER_IP]
- Sandbox: bc-sandbox.yourdomain.com → [SANDBOX_SERVER_IP]
 
### SSL/TLS Certificates
- Production: [CERT_THUMBPRINT]
- Sandbox: [CERT_THUMBPRINT]
- Expiry: [CERT_EXPIRY_DATE]
 
## Service Account Details
- **Production Service Account**: [DOMAIN\BC-PROD-SVC]
- **Sandbox Service Account**: [DOMAIN\BC-SANDBOX-SVC]
- **SQL Service Account**: [DOMAIN\SQL-SVC]
 
## Maintenance Windows
- **Production**: Sunday 2:00 AM - 6:00 AM
- **Sandbox**: Any time (notify users 24h advance)
 
## Emergency Contacts
- **BC Administrator**: [NAME] - [EMAIL] - [PHONE]
- **Azure Cloud Administrator**: [NAME] - [EMAIL] - [PHONE]
- **Customer IT Administrator**: [NAME] - [EMAIL] - [PHONE]
