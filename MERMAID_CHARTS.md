# TWiST Beauty Team Structure - Mermaid Charts

This repository contains interactive Mermaid.js organizational charts for TWiST Beauty's team structure. These charts can be imported and used in GitHub, documentation, or any Mermaid-compatible platform.

## 📊 Available Charts

### 1. Organization Overview
Complete organizational structure showing all team members and their relationships.

```mermaid
graph TD
    CEO[Nunya Seshie Tomey<br/>Chief Executive Officer]
    CMO[Tina Delasi Zigah<br/>Chief Marketing Officer]
    CPO[Mawuli Kwadzofio<br/>Chief Product Officer]
    CTO[Samuel Twumasi<br/>Chief Technology Officer]
    
    PD[Prince Osei<br/>Product Designer]
    GD[Cyril Kwame Ashiabi<br/>Graphic Designer]
    MD[Prince Cyprian<br/>Motion Designer]
    DM[Ayoola<br/>Digital Marketing Support]
    
    SM[Betty<br/>Social Media Intern]
    RM1[Francis Jones Akonnor<br/>Relationship Manager Intern]
    RM2[Jael<br/>Relationship Manager Intern]
    MG[Margaret<br/>Marketing & Customer Growth]
    
    CEO --- CMO
    CEO --- CPO
    CEO --- CTO
    
    CMO --- DM
    CMO --- SM
    CMO --- MG
    
    CPO --- PD
    CPO --- GD
    CPO --- MD
    
    CTO --- RM1
    CTO --- RM2
    
    classDef ceo fill:#E91E63,stroke:#8E24AA,stroke-width:3px,color:#fff
    classDef csuite fill:#8E24AA,stroke:#E91E63,stroke-width:2px,color:#fff
    classDef core fill:#10B981,stroke:#065F46,stroke-width:2px,color:#fff
    classDef intern fill:#F59E0B,stroke:#92400E,stroke-width:2px,color:#fff
    
    class CEO ceo
    class CMO,CPO,CTO csuite
    class PD,GD,MD,DM core
    class SM,RM1,RM2,MG intern
```

### 2. Reporting Structure
Clear hierarchy showing direct reporting relationships.

```mermaid
graph TD
    CEO[CEO<br/>Nunya Seshie Tomey]
    
    CEO --> CMO[CMO<br/>Tina Delasi Zigah]
    CEO --> CPO[CPO<br/>Mawuli Kwadzofio]
    CEO --> CTO[CTO<br/>Samuel Twumasi]
    
    CMO --> DM[Ayoola<br/>Digital Marketing]
    CMO --> SM[Betty<br/>Social Media Intern]
    CMO --> MG[Margaret<br/>Marketing & Growth]
    
    CPO --> PD[Prince Osei<br/>Product Designer]
    CPO --> GD[Cyril Ashiabi<br/>Graphic Designer]
    CPO --> MD[Prince Cyprian<br/>Motion Designer]
    
    CTO --> RM1[Francis Akonnor<br/>Relationship Manager]
    CTO --> RM2[Jael<br/>Relationship Manager]
    
    classDef ceo fill:#E91E63,stroke:#8E24AA,stroke-width:4px,color:#fff
    classDef executive fill:#8E24AA,stroke:#E91E63,stroke-width:3px,color:#fff
    classDef team fill:#10B981,stroke:#065F46,stroke-width:2px,color:#fff
    classDef intern fill:#F59E0B,stroke:#92400E,stroke-width:2px,color:#fff
    
    class CEO ceo
    class CMO,CPO,CTO executive
    class PD,GD,MD,DM team
    class SM,RM1,RM2,MG intern
```

### 3. Communication Flows & Role Interactions
Interactive diagram showing how team members collaborate, communicate, and share responsibilities across departments.

```mermaid
graph LR
    subgraph "Executive Leadership"
        CEO[CEO<br/>Nunya Seshie Tomey]
        CMO[CMO<br/>Tina Delasi Zigah]
        CPO[CPO<br/>Mawuli Kwadzofio]
        CTO[CTO<br/>Samuel Twumasi]
    end
    
    subgraph "Creative & Design Team"
        PD[Prince Osei<br/>Product Designer]
        GD[Cyril Ashiabi<br/>Graphic Designer]
        MD[Prince Cyprian<br/>Motion Designer]
    end
    
    subgraph "Marketing & Growth"
        DM[Ayoola<br/>Digital Marketing]
        SM[Betty<br/>Social Media Intern]
        MG[Margaret<br/>Marketing Specialist]
    end
    
    subgraph "Customer Relations"
        RM1[Francis Akonnor<br/>Relationship Manager]
        RM2[Jael<br/>Relationship Manager]
    end
    
    %% Executive Communications
    CEO -.->|Strategic Direction| CMO
    CEO -.->|Product Vision| CPO
    CEO -.->|Tech Strategy| CTO
    
    %% Cross-functional Collaborations
    CMO <-->|Campaign Planning| CPO
    CPO <-->|Design Requirements| PD
    PD <-->|Visual Assets| GD
    GD <-->|Motion Graphics| MD
    
    %% Marketing Communications
    CMO -->|Marketing Strategy| DM
    DM <-->|Content Creation| SM
    DM <-->|Growth Analytics| MG
    
    %% Design-Marketing Bridge
    PD -.->|Brand Guidelines| DM
    GD <-->|Marketing Materials| SM
    MD -.->|Video Content| DM
    
    %% Customer Feedback Loop
    CTO -->|Customer Insights| RM1
    CTO -->|Support Strategy| RM2
    RM1 -.->|User Feedback| PD
    RM2 -.->|Customer Data| MG
    
    %% Quality & Brand Alignment
    CMO -.->|Brand Standards| GD
    CPO -.->|Design Review| MD
    CEO -.->|Final Approval| CMO
    
    classDef executive fill:#E91E63,stroke:#8E24AA,stroke-width:3px,color:#fff
    classDef creative fill:#8E24AA,stroke:#E91E63,stroke-width:2px,color:#fff
    classDef marketing fill:#10B981,stroke:#065F46,stroke-width:2px,color:#fff
    classDef relations fill:#F59E0B,stroke:#92400E,stroke-width:2px,color:#fff
    
    class CEO,CMO,CPO,CTO executive
    class PD,GD,MD creative
    class DM,SM,MG marketing
    class RM1,RM2 relations
```

## 🎨 Color Coding System

| Role Level | Color | Description |
|------------|-------|-------------|
| **CEO** | Pink (#E91E63) | Chief Executive Leadership |
| **C-Suite** | Purple (#8E24AA) | Chief Marketing, Product, Technology Officers |
| **Core Team** | Green (#10B981) | Product Designers, Marketing Specialists |
| **Interns** | Orange (#F59E0B) | Relationship Managers, Social Media Interns |

## 📋 Communication Legend

| Symbol | Meaning |
|--------|---------|
| `-->` | Direct Reports & Strategy |
| `-.->` | Collaboration & Feedback |
| `<-->` | Two-way Communication |

## 🚀 Usage Instructions

### GitHub Integration
1. Copy any chart code block from above
2. Paste into your GitHub README.md or documentation
3. The chart will render automatically in GitHub's Mermaid support

### Documentation Sites
- **GitBook**: Supports Mermaid charts natively
- **Notion**: Use Mermaid code blocks
- **Confluence**: Install Mermaid plugin
- **GitLab**: Native Mermaid support in markdown

### Development Environments
```html
<!-- Include Mermaid.js in your HTML -->
<script src="https://cdn.jsdelivr.net/npm/mermaid@10.6.1/dist/mermaid.min.js"></script>

<!-- Chart container -->
<div class="mermaid">
  <!-- Paste chart code here -->
</div>

<!-- Initialize -->
<script>
  mermaid.initialize({
    startOnLoad: true,
    theme: 'base',
    themeVariables: {
      primaryColor: '#E91E63',
      primaryTextColor: '#ffffff',
      primaryBorderColor: '#8E24AA'
    }
  });
</script>
```

## 📁 Team Structure Summary

### Executive Leadership (4 members)
- **CEO**: Nunya Seshie Tomey - Overall strategy and leadership
- **CMO**: Tina Delasi Zigah - Marketing and brand strategy
- **CPO**: Mawuli Kwadzofio - Product development and design oversight
- **CTO**: Samuel Twumasi - Technology and customer relations

### Core Team (4 members)
- **Product Designer**: Prince Osei - UI/UX and product design
- **Graphic Designer**: Cyril Kwame Ashiabi - Visual identity and graphics
- **Motion Designer**: Prince Cyprian - Animation and motion graphics
- **Digital Marketing**: Ayoola - Online marketing and campaigns

### Interns & Growth (4 members)
- **Social Media Intern**: Betty - Social media management
- **Relationship Manager**: Francis Jones Akonnor - Customer relationships
- **Relationship Manager**: Jael - Customer support and engagement
- **Marketing & Growth**: Margaret - Marketing analysis and growth strategies

### Support Members (8 members)
Part-time contributors: Doreen, Jude, Rosalinda, Jessica, Mimi, Ella, Louis, Mavelli

## 🔗 Key Cross-functional Areas

1. **Brand & Creative Alignment**: CMO → CPO → Design Team
2. **Product-Marketing Bridge**: Product Designers ↔ Marketing Team
3. **Customer Feedback Loop**: Relationship Managers → Product/Marketing
4. **Content Creation Pipeline**: Design → Motion → Marketing Distribution

## 📞 Contact & Updates

For questions about team structure or chart updates, contact the executive team through official TWiST Beauty channels.

Last updated: January 2024