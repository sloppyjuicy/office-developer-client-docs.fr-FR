---
title: Documentation du développeur Project 2013
manager: soliver
ms.date: 04/04/2016
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
- vue d’ensemble de project 2013, Project 2013, Kit de développement logiciel SDK
localization_priority: Normal
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: Recherchez la documentation, exemples de code, articles explicatifs et références de programmation pour aider à créer des applications pour l’Office Store ou un catalogue d’applications privé et à personnaliser et à intégrer les clients Project et Project Server avec une grande variété d’autres du bureau et d’entreprise applications de gestion de projet d’entreprise.
ms.openlocfilehash: 490b5bd2fcbe2f92653b6ebc84d36e5c28cdc8c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787926"
---
# <a name="project-2013-developer-documentation"></a>Documentation du développeur Project 2013

Recherchez la documentation, exemples de code, articles explicatifs et références de programmation pour aider à créer des applications pour l’Office Store ou un catalogue d’applications privé et à personnaliser et à intégrer les clients Project et Project Server avec une grande variété d’autres du bureau et d’entreprise applications de gestion de projet d’entreprise.
  
Bienvenue dans le Microsoft Project 2013 Kit de développement logiciel (SDK). Le Kit de développement contient la documentation, des exemples de code, articles explicatifs et références de programmation pour aider à créer des applications pour une banque de dossiers publics ou un catalogue d’applications privé et à personnaliser et à intégrer Project Server et les clients Project avec une grande variété d’autres bureau et applications d’entreprise pour la gestion de projet d’entreprise.
  
> [!NOTE]
> Project Server 2013 repose sur la plateforme SharePoint Server 2013 et Project 2013 présente l’essentiel de la même infrastructure que les autres applications Office 2013. Pour la documentation du modèle pour SharePoint Add-ins, flux de travail basées sur SharePoint, des composants WebPart, développement avec d’autres fonctionnalités SharePoint et de la documentation des compléments Office, voir [Apps for Office et SharePoint](http://msdn.microsoft.com/en-us/library/fp161507%28office.15%29.aspx). 
  
## <a name="introduction-to-the-project-sdk"></a>Présentation du kit de développement logiciel Project
<a name="pj15_Welcome_IntroToSDK"> </a>

Project Server 2013 est une plateforme pour la création de solutions de gestion de projet local ou entreprise basée sur le cloud et à la création d’applications que les utilisateurs finaux peuvent découvrir et d’obtenir via une banque publique ou un catalogue d’applications privé. L’architecture de Project Server 2013 est basé sur la plateforme introduite dans Microsoft Office Project Server 2007 avec nombreuses nouvelles fonctionnalités et améliorations. Les nouvelles fonctionnalités incluent un modèle objet côté client (CSOM) pour activer l’accès à Project Online, un service OData pour l’accès en ligne aux rapports de données, des récepteurs d’événements distants, architecture de flux de travail est basé sur la version 4 du flux de travail Windows de Project Server Foundation (WF4) et des compléments Office, qui est une architecture commune pour les extensions de volet de tâches dans les applications clientes Microsoft Office 2013.
  
Une modification majeure de Project Server 2013 est l’utilisation d’une base de données à la place les bases de données brouillon, publiée, archivage et création de rapports dans Project Server 2010. Pour plus d’informations sur les nouvelles fonctionnalités et les fonctionnalités déconseillées, voir [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md). Pour plus d’informations sur les modifications apportées à la plateforme de Project Server, consultez [architecture de Project Server 2013](project-server-2013-architecture.md). Pour une vue d’ensemble de la plateforme de développement qui existe dans Project Server 2010 et Project Server 2013 basé sur, voir [Mise en route avec le développement pour Project 2010](http://msdn.microsoft.com/en-us/library/gg607685.aspx) sur MSDN. 
  
Project Server 2013 repose sur le Microsoft .NET Framework 4 et Microsoft SharePoint Server 2013. Les articles et les exemples dans ce SDK fournissent un point de départ pour le développement de solutions personnalisées et des applications ; ils ne concernent pas toutes les fonctionnalités de la programmabilité de Project Server ou Project Professionnel. Le [Centre de développement Project](http://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx) inclut des liens vers les articles Project, blogs, vidéos, webcasts, des articles de procédures visual et autres ressources. 
  
Le Kit de développement Project 2013 contient des informations de développement pour Project Server 2013, Project Web App, Project Professional 2013 et Project Standard 2013. Les articles SDK sont conçus pour aider les développeurs et les administrateurs évaluer Project et Project Server pour l’extensibilité et de planifier des solutions personnalisées.
  
### <a name="feedback"></a>Commentaires
<a name="pj15_Welcome_Feedback"> </a>

Nous aimerions entendre. Dans les rubriques online sur MSDN, vous pouvez ajouter des commentaires, des exemples de code, ou marquer le contenu comme un bogue dans la section **Contenu de la Communauté** en bas de chaque page. Lorsque vous installez le téléchargement du Kit de développement Project 2013, les articles de locale documentation ont un lien *d’Envoyer des commentaires* qui se trouve au-dessous du titre. À tout moment dans le Kit de développement logiciel de lecture, cliquez sur le lien pour envoyer un message électronique à l’équipe SDK. Vous pouvez envoyer des corrections, une demande pour clarification ou un exemple de code ou autres commentaires et faciliter le contenu plus facilement distingué. 
  
### <a name="download"></a>Téléchargement
<a name="pj15_Welcome_Download"> </a>

Le téléchargement du Kit de développement Project 2013 est disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20) ( `https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`). Le téléchargement inclut Project2013SDK.HxS (le fichier qui contient cet article), les exemples de code, assemblys redistribuables et autres ressources. Le Kit de développement Project 2013 n’inclut pas encore la référence de tables de données de création de rapports.
  
### <a name="whats-new-in-the-project-sdk"></a>Nouveautés du kit de développement logiciel Project
<a name="pj15_Welcome_WhatsNew"> </a>

L’objectif principal du Kit de développement Project 2013 est de fournir une vue d’ensemble de la programmabilité et la documentation des CSOM et des fonctionnalités associées pour la création d’applications, services Project Server Interface (PSI), les applications de volet de tâches pour Project Professionnel 2013. Le Kit de développement Project 2013 inclut des exemples pas à pas de zones clés pour la personnalisation de Project Server 2013 et les clients de projet (Project Standard 2013, Project Professional 2013 et Project Web App). La documentation est incomplète ; plus de contenu seront ajoutées dans les versions ultérieures. 
  
La technologie sous-jacente pour la communication réseau est Windows Communication Foundation (WCF) de Project Server 2013, y compris de scénarios de nuage qui utilisent la Project Server CSOM et au développement localement à l’aide de l’interface PSI. Les références de service web ASMX hérités sont également basés sur l’architecture WCF. Définition d’une référence à un service web PSI (fichier ASMX) dans Project Server 2013 requiert l’ajout de la `?wsdl` option d’URL pour le chemin d’accès. Par exemple, `http://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`.
  
> [!NOTE]
> Bien qu’il traite uniquement les fonctionnalités de Project Server les plus fréquemment utilisées, nous vous conseillons d’utiliser le modèle CSOM lorsque cela est possible pour les applications à la fois sur site et dans le nuage. Bien qu’il soit toujours disponible dans Project Server 2013, l’interface ASMX pour l’interface PSI est déconseillée. Pour les applications locales qui nécessitent un accès complet à l’interface PSI, vous devez utiliser l’interface WCF pour l’interface PSI, plutôt que l’interface ASMX. 
  
Développement sur un ordinateur Windows 7 est pris en charge en copiant les assemblys CSOM pour Project Server 2013 et SharePoint Server 2013 vers l’ordinateur de développement. Le téléchargement du kit SDK comprend les assemblys CSOM pour Project Server et une licence de redistribution. Pour obtenir des assemblys SharePoint CSOM, voir [Le SDK des composants Client SharePoint Server 2013](http://www.microsoft.com/en-us/download/details.aspx?id=35585).
  
Pour le développement avec les services WCF, vous pouvez définir une référence sur un assembly de proxy PSI ou ajouter des fichiers proxy PSI à la solution. Vous pouvez définir des références directes sur les services web Project Server ASMX frontaux depuis un ordinateur distant dans le même domaine, ou utiliser un assembly de proxy ou des fichiers de proxy. Le téléchargement du kit de développement logiciel inclut des fichiers de proxy pour les services WCF et les services web ASMX, ainsi que des scripts pour la création d’assemblies de proxy et la génération de fichiers de proxy mis à jour.
  
Dans Project Server 2013, vous pouvez créer des flux de travail déclaratifs Project Server à l’aide de Microsoft SharePoint Designer 2013 pour les deux local et utiliser en ligne. SharePoint Designer 2013 utilise les méthodes et propriétés d’activité de flux de travail dans le modèle CSOM. Développement et déploiement de solutions Visual Studio 2012 qui incluent des composants WebPart Project Server ou les personnalisations de Project Web App, est pris en charge uniquement sur un ordinateur de Project Server.
  
Pour une vue d’ensemble des nouvelles fonctionnalités de programmabilité et les fonctionnalités déconseillées de Project Server 2013, voir [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md). Une autre modification importante dans Project Server 2013 est l’utilisation de flux de travail WF4 pour gérer la création et l’approbation des propositions de projet qui sont basés sur les modèles de projet d’entreprise. 
  
Voici quelques-unes des nouvelles rubriques :
  
- [Créer un serveur de Project Server hébergée sur SharePoint complément](create-a-sharepoint-hosted-project-server-add-in.md) montre comment utiliser Visual Studio pour le développement à distance d’une application qui peut être utilisé avec Project Server 2013 et Project Online. 
    
- [Architecture de Project Server 2013](project-server-2013-architecture.md) explique les nouvelles fonctionnalités principales de la plateforme de Project Server. 
    
- [Mise en route avec le modèle objet Project Server 2013 JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md) montre comment développer des applications web qui peuvent accéder à Project Server. 
    
- [Mise en route avec Project Server CSOM et .NET](getting-started-with-the-project-server-csom-and-net.md) montre comment utiliser le modèle objet côté client pour développer des applications, au lieu d’utiliser les services PSI. 
    
- [Applications du volet Office pour Project Professionnel](task-pane-add-ins-for-project.md) présente les compléments Office, comme appliqué à Project 2013. Le Kit de développement Office 2013 comprend des articles qui montrent comment développer des applications de volet de tâches pour Project et les autres clients Office 2013. 
    
- [Créer un flux de travail Project Server pour la gestion de la demande](create-a-project-server-workflow-for-demand-management.md) montre comment SharePoint Designer 2013 peut être utilisée pour créer des flux de travail Project Server. 
    
- [ProjectData - référence de service OData Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx) inclut une vue d’ensemble de l’interface OData pour les rapports de Project Server, ainsi que des rubriques de référence XML pour le service **ProjectData** . 
    
Les rubriques de l’espace de noms **Microsoft.ProjectServer.Client** et les nouvelles méthodes dans les services PSI ont uniquement une documentation minimale. La plupart des rubriques de référence pour les services PSI sont identiques par rapport à la version de juillet 2011 du Kit de développement Project 2010. 
  
### <a name="future-sdk-releases"></a>Versions du kit de développement logiciel à venir
<a name="pj15_Welcome_FutureReleases"> </a>

Le Kit de développement Project 2013 à jour avec nouveaux articles et de contenu de référence pour la version de disponibilité générale.
  
## <a name="sections-in-the-project-sdk"></a>Sections du kit de développement logiciel Project
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Il existe deux sections de niveau supérieur dans le Kit de développement Project 2013 :
  
- La section [d’articles d’informations conceptuelles et procédures Project](project-conceptual-and-how-to-articles.md) contient des vues d’ensemble des principales fonctionnalités et des articles de procédures pas à pas pour le développement. 
    
- La section [référence service Project Server 2013 classe web et de la bibliothèque de](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) documents au modèle objet des assemblys publics, l’assembly Microsoft.ProjectServer.Client.dll pour le modèle CSOM et les services PSI. 
    
La section **concepts et procédures** inclut les éléments suivants : 
  
- [Quelles sont les nouveautés et composants disponibles pour les développeurs](updates-for-developers-in-project-2013.md) décrit les nouvelles fonctionnalités de programmabilité principales et les fonctionnalités déconseillées dans Project 2013. 
    
- [Vue d’ensemble du projet pour les développeurs](http://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx) contient des articles sur l’architecture de Project Server, articles expliquant comment commencer à développer avec le modèle CSOM et une référence à la SDK Office 2013, qui contient plus d’informations sur les nouvelles fonctionnalités dans VBA pour Project rubriques sur le développement d’applications du volet Office pour Project Professionnel 2013. 
    
- [Tâches de programmation de projet](project-programming-tasks.md) inclut les articles de procédures sur la création d’applications pour Project Server, l’utilisation de JavaScript avec le modèle CSOM et création des propositions de projets et des flux de travail pour la gestion de la demande. 
    
- [Références de programmation de Project 2013](project-2013-programming-references.md) comprend une introduction à la documentation de référence PSI pour la référence du schéma pour le service **ProjectData** OData, informations sur les codes d’erreur de Project Server et Project Server 2013. 
    
> [!NOTE]
>  Configuration minimale requise pour développer et déployer des applications à partir de l’Office Store public intégrant avec Project Server 2013 et solutions EPM : > vous devez installer le .NET Framework 4 ou le .NET Framework 4.5 sur l’ordinateur de développement et le déploiement ordinateurs. Pour déterminer si la version correcte est installée, ouvrez **programmes et fonctionnalités** dans le panneau de configuration Windows. > Visual Studio 2012 installe et utilise le .NET Framework 4.5. Lorsque vous créez un projet Visual Studio, vous pouvez sélectionnez **.NET Framework 4.0** ou **NET Framework 4.5** dans la liste déroulante de la boîte de dialogue **Nouveau projet** . Vous pouvez également sélectionner le **Framework cible** sous l’onglet **Application** de la fenêtre **Propriétés** du projet. > Vous pouvez utiliser Visual Studio 2010 pour les applications qui utilisent le modèle CSOM et PSI et pour les applications de volet de tâches de projet. Toutefois, Visual Studio 2010 ne contient pas les modèles de compléments Office, outils de développement Office ou les outils de développement SharePoint pour Office 2013. Pour télécharger Visual Studio 2012 et Web Platform Installer (WebPI) qui inclut les outils de développement Office et SharePoint, consultez les [téléchargements pour les applications pour Office et SharePoint](http://msdn.microsoft.com/en-us/office/apps/fp123627). > Il est recommandé de développer des solutions personnalisées dans un environnement de test. Si vous développez des solutions en cours pour les versions de Project Server 2013 et Project 2013, ils doivent être recompilées avec références mises à jour et peuvent nécessiter des modifications supplémentaires, pour travailler avec les versions ultérieures. Solutions développées pour toute version précommerciale peuvent ne pas fonctionnent avec la version finale. 
  
## <a name="see-also"></a>Voir aussi
<a name="pj15_Welcome_AR"> </a>

- [Mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md)
    
- [Architecture de Project Server 2013](project-server-2013-architecture.md)
    
- [Téléchargement du Kit de développement logiciel (SDK) de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Kit de développement de composants SharePoint Server 2013 Client](http://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [Projet pour les développeurs](http://msdn.microsoft.com/project)
    
- [Documentation du développeur Office](http://msdn.microsoft.com/office)
    
- [Mise en route avec le développement pour Project 2010](http://msdn.microsoft.com/en-us/library/gg607685.aspx)
    
- [Conventions de document](http://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [Accessibilité dans les produits SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj841103.aspx)
    
- [Accessibilité dans Microsoft Office 365](http://www.microsoft.com/enable/products/office365/)
    
- [Confidentialité en ligne de Microsoft](https://privacy.microsoft.com/en-us/privacystatement)
    

