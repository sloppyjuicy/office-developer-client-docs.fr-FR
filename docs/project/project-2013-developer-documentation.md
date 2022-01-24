---
title: Documentation du développeur Project 2013
manager: lindalu
ms.date: 09/19/2021
ms.audience: Developer
f1_keywords:
- Project
- Project 2013
- Project 2013 SDK
- Project programmability
- Project SDK
- SDK
- SDK Project
keywords:
- Kit de développement logiciel, Project 2013, Project 2013, vue d’ensemble du kit de développement logiciel
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: Trouvez de la documentation, des exemples de code, des articles pratiques et des références de programmation pour vous aider à créer des applications pour Office ou un catalogue d’applications privé, et à personnaliser et intégrer des clients Project et Project Server avec une grande variété d’autres applications de bureau et d’entreprise pour la gestion de projet d’entreprise.
ms.localizationpriority: high
ms.openlocfilehash: 2b4b646243a9eb84543eb0669b5ed500ad82b7f2
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180655"
---
# <a name="project-2013-developer-documentation"></a>Documentation du développeur Project 2013

Recherchez de la documentation, des exemples de code, des articles pratiques et des références de programmation pour vous aider à créer des applications pour AppSource. Découvrez comment personnaliser et intégrer Project Server et les clients Project à un large éventail d’autres applications de bureau et métier pour la gestion de projet d’entreprise (EPM).
   
> [!NOTE]
> Project Server 2013 est basé sur la plateforme SharePoint Server 2013 et Project 2013 inclut pratiquement la même infrastructure que les autres applications Office 2013. Pour la documentation du modèle pour les compléments SharePoint, les flux de travail SharePoint, les composants WebPart, le développement avec d’autres fonctionnalités de SharePoint et la documentation des compléments Office, consultez [Compléments SharePoint](/sharepoint/dev/sp-add-ins/sharepoint-add-ins.md) et [Compléments Office](/office/dev/add-ins/overview/office-add-ins.md). 
  
## <a name="introduction-to-the-project-software-development-kit-sdk"></a>Présentation du kit de développement logiciel (SDK) Project

Project Server 2013 est une plateforme permettant de créer des solutions de gestion de projet d’entreprise en local ou sur le cloud et des applications que les utilisateurs finaux peuvent découvrir et acquérir via AppSource (précédemment appelé Office Store). L’architecture de Project Server 2013 est basée sur la plateforme introduite dans Microsoft Office Project Server 2007, avec de nombreux ajouts et améliorations. Les nouvelles fonctionnalités incluent un modèle objet côté client (CSOM) pour activer l’accès à Project Online, un service OData pour l’accès en ligne aux données de création de rapports de Project Server, des récepteurs d’événements à distance, une architecture de flux de travail basée sur la version 4 de Windows Workflow Foundation (WF4) et des compléments Office, qui est une architecture courante pour les extensions de volet de tâches dans les applications clientes Microsoft Office 2013.
  
Un changement majeur dans Project Server 2013 est l’utilisation d’une base de données unique à la place des bases de données provisoire, publiée, d’archivage et de création de rapports dans Project Server 2010. Pour plus d’informations sur les nouvelles fonctionnalités et les fonctionnalités déconseillées, consultez la rubrique relative aux [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md). Pour plus d’informations sur les modifications dans la plateforme Project Server, consultez la rubrique relative à l’[architecture Project Server 2013](project-server-2013-architecture.md). Pour une vue d’ensemble de la plateforme de développement qui existe dans Project Server 2010 et sur laquelle Project Server 2013 est basé, consultez la rubrique relative à la [prise en main du développement pour Project 2010](https://msdn.microsoft.com/library/gg607685.aspx) sur MSDN. 
  
Project Server 2013 est créé sur Microsoft .NET Framework 4 et Microsoft SharePoint Server 2013. Les articles et exemples de ce kit de développement logiciel fournissent un point de départ pour le développement de solutions et d’applications personnalisées. Ils ne traitent pas toutes les fonctionnalités de programmation de Project Server ou Project Professionnel. Le [Centre de développement Project](https://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx) inclut des liens vers des articles, des blogs, des vidéos, des présentations techniques en ligne, des articles pratiques visuels et d’autres ressources Project. 
  
Le kit de développement logiciel Project 2013 inclut des informations destinées aux développeurs pour Project Server 2013, Project Web App, Project Professionnel 2013 et Project Standard 2013. Les articles de kit de développement logiciel sont conçus pour aider les développeurs et les administrateurs à évaluer l’extensibilité de Project et Project Server, et à planifier des solutions personnalisées.
  
### <a name="welcome-feedback"></a>Commentaires de bienvenue

Vos commentaires sont les bienvenus. Dans les rubriques en ligne sur MSDN, vous pouvez ajouter des commentaires, des exemples de code ou marquer le contenu comme bogue dans la section **Contenu de la communauté** en bas de chaque page. Lorsque vous installez le téléchargement du kit de développement logiciel (SDK) Project 2013, les articles de la documentation locale ont un lien *Envoyer des commentaires* sous le titre. À tout moment de la lecture du kit de développement logiciel, cliquez sur le lien pour envoyer un e-mail à l’équipe du kit de développement logiciel. Vous pouvez envoyer des corrections, une demande de clarification ou un exemple de code, ou d’autres commentaires pour nous aider à améliorer le contenu. 
  
### <a name="download"></a>Téléchargement

Le téléchargement du kit de développement logiciel (SDK) de Project 2013 est disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=30435%20) (`https://www.microsoft.com/download/details.aspx?id=30435%20`). Le téléchargement inclut Project2013SDK.HxS (le fichier qui inclut cet article), les exemples de code associés, les assemblys redistribuables et d’autres ressources. Le kit de développement logiciel Project 2013 n’inclut pas encore la référence des tables de bases de données de création de rapports.
  
### <a name="whats-new-in-the-project-sdk"></a>Nouveautés du kit de développement logiciel Project
<a name="pj15_Welcome_WhatsNew"> </a>

L’objectif principal du kit de développement logiciel Project 2013 est de fournir une vue d’ensemble de la programmabilité et la documentation du CSOM et des fonctionnalités connexes pour la création d’applications, des services de l’Interface Project Server (PSI) et des applications de volet de tâches pour Project Professionnel 2013. Le kit de développement logiciel Project 2013 inclut des exemples détaillés des domaines clés pour la personnalisation de Project Server 2013 et des clients Project (Project Standard 2013, Project Professionnel 2013 et Project Web App). La documentation est incomplète ; davantage de contenu sera ajouté dans les versions ultérieures. 
  
La technologie sous-jacente pour la communication réseau est Windows Communication Foundation (WCF) dans Project Server 2013, comprenant des scénarios cloud qui utilisent le modèle CSOM Project Server et le développement local à l’aide de l’interface PSI. Les références du service web ASMX héritées sont également basées sur l’architecture WCF. La définition d’une référence à un service web PSI (fichier ASMX) dans Project Server 2013 nécessite l’ajout de l’option d’URL `?wsdl` au chemin d’accès. Par exemple : `https://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`.
  
> [!NOTE]
> Même s’il traite uniquement les fonctionnalités de Project Server les plus fréquemment utilisées, nous vous conseillons d’utiliser le modèle CSOM chaque fois que vous le pouvez pour les applications en local et dans le cloud. Même si elle est toujours disponible dans Project Server 2013, l’interface ASMX pour l’interface PSI est déconseillée. Pour les applications en local qui nécessitent un accès complet à l’interface PSI, vous devez utiliser l’interface WCF pour l’interface PSI, au lieu de l’interface ASMX. 
  
Le développement sur un ordinateur Windows 7 est pris en charge en copiant les assemblys CSOM pour Project Server 2013 et SharePoint Server 2013 sur l’ordinateur de développement. Le téléchargement du kit de développement logiciel inclut les assemblys CSOM pour Project Server et une licence de redistribution. Pour obtenir les assemblys CSOM SharePoint, reportez-vous à l’article relatif au [kit de développement logiciel des composants du client SharePoint Server 2013](https://www.microsoft.com/download/details.aspx?id=35585).
  
Pour le développement avec les services WCF, vous pouvez définir une référence sur un assembly de proxy PSI ou ajouter des fichiers proxy PSI à la solution. Vous pouvez définir des références directes sur les services web Project Server ASMX frontaux depuis un ordinateur distant dans le même domaine, ou utiliser un assembly de proxy ou des fichiers de proxy. Le téléchargement du kit de développement logiciel inclut des fichiers de proxy pour les services WCF et les services web ASMX, ainsi que des scripts pour la création d’assemblies de proxy et la génération de fichiers de proxy mis à jour.
  
Dans Project Server 2013, vous pouvez créer des flux de travail Project Server déclaratifs à l’aide de Microsoft SharePoint Designer 2013 pour une utilisation locale et en ligne. SharePoint Designer 2013 utilise les méthodes et les propriétés d’activité de flux de travail dans le modèle CSOM. Le développement et le déploiement des solutions Visual Studio 2012 qui incluent des composants WebPart Project Server, ou des personnalisations de Project Web App, sont pris en charge uniquement sur un ordinateur Project Server.
  
Pour une vue d’ensemble des nouvelles fonctionnalités de programmabilité et des fonctionnalités déconseillées dans Project Server 2013, reportez-vous à la rubrique relative aux [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md). Une autre modification majeure dans Project Server 2013 est l’utilisation de flux de travail basés sur WF4 pour gérer la création et l’approbation de propositions de projet basées sur des modèles de projet d’entreprise. 
  
Voici quelques-unes des nouvelles rubriques :
  
- Rubrique décrivant comment [créer un complément Project Server hébergé par SharePoint](create-a-sharepoint-hosted-project-server-add-in.md) qui explique comment utiliser Visual Studio pour le développement distant d’une application pouvant être utilisée avec Project Server 2013 et Microsoft Project Online. 
    
- Rubrique relative à l’[architecture Project Server 2013](project-server-2013-architecture.md) qui décrit les principales nouvelles fonctionnalités de la plateforme Project Server. 
    
- Rubrique relative à la [prise en main du modèle objet JavaScript Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) qui montre comment développer des applications web pouvant accéder à Project Server. 
    
- Rubrique relative à la [prise en main du modèle CSOM Project Server et de .NET](getting-started-with-the-project-server-csom-and-net.md) qui montre comment utiliser le modèle objet côté client pour développer des applications, au lieu d’utiliser les services PSI. 
    
- La rubrique relative aux [applications de volet de tâches pour Project Professionnel](task-pane-add-ins-for-project.md) présente les compléments Office, tels qu’appliqués à Project 2013. Le kit de développement logiciel Office 2013 inclut des articles qui décrivent le développement d’applications de volet de tâches pour Project et les autres clients Office 2013. 
    
- La rubrique relative à la [création d’un flux de travail Project Server pour la gestion de la demande](create-a-project-server-workflow-for-demand-management.md) décrit comment SharePoint Designer 2013 peut être utilisé pour créer des flux de travail Project Server. 
    
- La rubrique relative à la [référence de service ProjectData - Project OData](https://msdn.microsoft.com/library/office/jj163015.aspx) comprend une vue d’ensemble de l’interface OData pour la création de rapports Project Server, ainsi que des rubriques de référence XML pour le service **ProjectData**. 
    
Les rubriques dans l’espace de noms **Microsoft.ProjectServer.Client** et les nouvelles méthodes dans les services PSI ont une documentation minimale uniquement. La plupart des rubriques de référence pour les services PSI n’ont pas été modifiées depuis la version de juillet 2011 du kit de développement Project 2010. 
  
### <a name="future-sdk-releases"></a>Versions du kit de développement logiciel à venir

Le kit de développement logiciel Project 2013 sera mis à jour avec des nouveaux articles et contenu de référence pour la version de disponibilité générale.
  
## <a name="sections-in-the-project-sdk"></a>Sections du kit de développement logiciel Project

Il existe deux sections de niveau supérieur dans le kit de développement logiciel Project 2013 :
  
- La section relative aux [articles conceptuels et procédures liés à Project](project-conceptual-and-how-to-articles.md) contient des vues d’ensemble des principaux articles et fonctionnalités avec des procédures détaillées pour le développement. 
    
- La section relative à la [référence de service web et bibliothèque de classes Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) décrit le modèle objet des assemblys publics, l’assembly Microsoft.ProjectServer.Client.dll pour le modèle objet client et les services PSI. 
    
La section **Articles conceptuels et pratiques** comprend les éléments suivants : 
  
- [Nouveautés et éléments obsolètes pour les développeurs](updates-for-developers-in-project-2013.md) décrit les nouvelles fonctionnalités de programmabilité principales et les fonctionnalités déconseillées dans Project 2013. 
    
- La rubrique [Vue d’ensemble de Project pour les développeurs](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx) comprend des articles sur l’architecture de Project Server, des articles indiquant comment commencer à développer avec le modèle objet client, des informations sur les nouvelles fonctionnalités dans VBA pour Project et une référence au kit de développement logiciel Office 2013, qui contient des rubriques sur le développement d’applications de volet de tâches Project Professionnel 2013. 
    
- La rubrique relative aux [tâches de programmation Project](project-programming-tasks.md) comprend des articles pratiques sur la création d’applications pour Project Server, à l’aide de JavaScript avec le modèle objet client, et sur la création de propositions de projet et de flux de travail pour la gestion de la demande. 
    
- La rubrique relative aux [références de programmation Project 2013](project-2013-programming-references.md) comprend une présentation de la référence PSI pour Project Server 2013, des informations sur les codes d’erreur de Project Server et la référence de schéma OData pour le service **ProjectData**. 
    
> [!NOTE]
>  Voici les conditions requises pour développer et déployer des applications et des solutions EPM depuis l’AppSource qui s’intègrent avec Project Server 2013 : > Vous devez installer .NET Framework 4 ou .NET Framework 4.5 sur l’ordinateur de développement et sur les ordinateurs de déploiement. Pour déterminer si la version correcte est installée, ouvrez **Programmes et fonctionnalités** dans le Panneau de configuration Windows. > Visual Studio 2012 installe et utilise .NET Framework 4.5. Lorsque vous créez un projet Visual Studio, vous pouvez sélectionner **.NET Framework 4.0** ou **NET Framework 4.5** dans la liste déroulante de la boîte de dialogue **Nouveau projet**. Vous pouvez également sélectionner **Infrastructure cible** sur l’onglet **Application** de la fenêtre **Propriétés** du projet. > Vous pouvez utiliser Visual Studio 2010 pour les applications qui utilisent le modèle CSOM ou l’interface PSI, et pour les applications de volet de tâches Project. Cependant, Visual Studio 2010 ne contient pas les modèles de compléments Office, les outils de développement Office ou les outils de développement SharePoint pour Office 2013. Pour télécharger Visual Studio 2012 et le programme d’installation de la plateforme web (WebPI) qui inclut les outils de développement Office et SharePoint, reportez-vous à la section relative aux [téléchargements pour les applications pour Office et SharePoint](https://msdn.microsoft.com/office/apps/fp123627). > Nous vous recommandons de développer des solutions personnalisées dans un environnement de test. Si vous développez des solutions pour les versions actuelles de Project Server 2013 et Project 2013, elles doivent être recompilées avec des références mises à jour et peuvent avoir besoin de modifications supplémentaires, pour fonctionner avec des versions ultérieures. Les solutions développées pour n’importe quelle version préliminaire risquent de ne pas fonctionner avec la version finale. 
  
## <a name="see-also"></a>Voir aussi
<a name="pj15_Welcome_AR"> </a>

- [Mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md)
    
- [Architecture Project Server 2013](project-server-2013-architecture.md)
    
- [Téléchargement du kit de développement logiciel (SDK) de Project 2013](https://www.microsoft.com/download/details.aspx?id=30435%20)
    
- [Kit de développement logiciel (SDK) des composants du client SharePoint Server 2013](https://www.microsoft.com/download/details.aspx?id=35585)
    
- [Project pour les développeurs](https://msdn.microsoft.com/project)
    
- [Documentation pour les développeurs Office](https://msdn.microsoft.com/office)
    
- [Prise en main du développement pour Project 2010](https://msdn.microsoft.com/library/gg607685.aspx)
    
- [Conventions de document](https://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [Accessibilité dans SharePoint 2013](https://msdn.microsoft.com/library/jj841103.aspx)
    
- [Accessibilité dans Microsoft Office 365](https://www.microsoft.com/enable/products/office365/)
    
- [Déclaration de confidentialité Microsoft](https://privacy.microsoft.com/privacystatement)
    

