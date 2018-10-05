---
title: Architecture Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2cfa5a6e-2f5c-440c-b35a-bc7a34648f9c
description: Project Server 2013 intègre des fonctionnalités de gestion de projet au sein d’une batterie de serveurs SharePoint et permet l’utilisation de Project Online avec un modèle objet côté client (CSOM) et une interface OData pour les données de création de rapports.
ms.openlocfilehash: 633532d85b4d910c11a284231cb9a4c3e5a549cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394096"
---
# <a name="project-server-architecture"></a>Architecture Project Server

Project Server 2013 intègre des fonctionnalités de gestion de projet au sein d’une batterie de serveurs SharePoint et permet l’utilisation de Project Online avec un modèle objet côté client (CSOM) et une interface OData pour les données de création de rapports.
   
Project Server 2013 est un système multiniveau qui étend l’architecture introduite dans Office Project Server 2007. Les modifications architecturales incluent l’association du Service d’Application Project avec les collections de sites SharePoint, l’ajout de certains objets métiers sur le serveur web frontal (WFE), le modèle objet côté client (CSOM) pour l’accès distant, une base de données Project, un Interface OData pour les tables de création de rapports et affichages, l’intégration de Windows Workflow Foundation version 4 (WF4) par le biais de Workflow Manager Client 1.0 dans le nuage ou sur un serveur local et les récepteurs d’événements distants qui sont accessibles par plusieurs Project Server installations. En plus de solutions personnalisées sur site, vous pouvez créer des applications qui incluent des récepteurs d’événements distants et les composants accéder aux interfaces CSOM et OData.
  
Le niveau frontal inclut les applications tierces, Project Web App et Project Professional 2013. Les applications clientes communiquent avec la couche intermédiaire par le biais de l’Interface Project Server (PSI) ou via les points de terminaison CSOM, qui à son tour communiquent avec l’interface PSI et la couche des objets métiers. Accès aux données est intégré dans les objets métier. Le système d’événements Project Server peut accéder à la fois des gestionnaires d’événements locaux et des récepteurs d’événements distants. Le Service de calcul Project implémente le moteur de planification Project Professionnel dans Project Server. Applications clientes ne (ou non) accéder directement à la base de données de projet ; Project Server masque les objets métiers à partir de clients.
  
> [!NOTE]
> Project Server repose sur l’architecture de SharePoint. Pour plus d’informations sur le modèle d’application SharePoint et l’architecture de SharePoint Server 2013, consultez la section *mise en route avec le développement SharePoint* dans la documentation du développeur Office 2013. 

<a name="pj15_Architecture_SharePoint"> </a>

## <a name="integrating-with-sharepoint-site-collections"></a>Intégration aux collections de sites SharePoint

Le Service d’Application Project dans Project Server 2013 peut être associé à une collection de sites SharePoint pour une utilisation avec des listes de tâches SharePoint, le Service d’Application Project peut également importer une liste de tâches SharePoint en tant que projet d’entreprise pour complète de Project Server contrôle. Avec une liste de tâches SharePoint, SharePoint tient à jour le site de projet dans une collection de sites ; Project Professionnel peut synchroniser avec et mettre à jour la liste des tâches. Un site de projet peut être une liste de tâches SharePoint indépendante ou une liste de tâches qui est synchronisée avec un fichier .mpp ; le fichier .mpp peut être stocké localement ou dans une bibliothèque SharePoint. 
  
Project Server gère les projets lorsqu’il a le contrôle total ; Project Professional enregistre les données directement dans Project Server. Le tableau 1 compare le comportement d’une liste de tâches, le composant WebPart de planification et d’autres fonctionnalités pour le contrôle des listes de tâches SharePoint et des projets importés lorsque Project Server dispose du contrôle total. Le composant WebPart planification contient la grille dans la page de Project Web App dans laquelle vous pouvez modifier une planification de projet. Le mode de lié est où les données d’état sont inscrit qu’une seule fois pour les tâches et feuilles de temps ; dans le mode d’entrée unique, les données d’état de tâche sont entrées séparément à partir de feuilles de temps.
  
**Tableau 1. Comparaison des listes de tâches et du contrôle total SharePoint**

| Fonctionnalité | Liste des tâches | Contrôle total |
|:-----|:-----|:-----|
|**Liste des tâches SharePoint** <br/> |Lecture/écriture  <br/> |Lecture seule  <br/> |
|**Composant WebPart planification** <br/> |Lecture seule  <br/> |Lecture/écriture  <br/> |
|**Création de rapports** <br/> |Génération de rapports enrichie via Project Server  <br/> |Génération de rapports enrichie via Project Server  <br/> |
|**Autres fonctionnalités de Project Server** <br/> | Fonctionnalités bloquées :  <br/>Modifications de projet côté serveur, avec Project Web App ou des applications clientes personnalisées  <br/>-État  <br/>-Tâches ne sont pas visibles en mode lié  <br/> |Toutes les fonctionnalités sont activées  <br/> |
   
### <a name="managing-projects-as-sharepoint-task-lists"></a>Gestion de projets sous forme de listes des tâches SharePoint
<a name="pj15_Architecture_VisibilityMode"> </a>

Lorsque Project Server est associé à une collection de sites SharePoint où SharePoint gère le contrôle, listes de tâches et les fichiers de Project Professionnel 2013 (.mpp) dans les bibliothèques de documents sont visibles par le Service d’Application Project, mais SharePoint tient à jour le maîtriser les données pour la synchronisation (voir Figure 1). Planification côté serveur avec le composant WebPart de planification ne peut pas être effectuée. Vous pouvez utiliser Project Professional pour se synchroniser avec et modifier la liste des tâches dans un site de projet. En commençant par les listes de tâches SharePoint, les organisations peuvent évoluer progressivement pour utiliser l’ensemble des fonctionnalités de Project Server.
  
La figure 1 illustre les processus suivants lorsque les projets sont tenus à jour dans des listes de tâches SharePoint : 
  
- (A) Project Professionnel peut synchroniser la liste des tâches et créer des sites de projet dans la collection de sites avant ou après l’association avec le service d’application Project.
    
- (B) Project Server synchronise les données du site de projet à des fins de génération de rapports, mais SharePoint tient à jour les données de base ; les listes des tâches restent en lecture/écriture.
    
- (C) Après l’association, Project Professionnel peut créer des projets et les enregistrer ou les publier dans Project Server. Le cache actif dans Project Professionnel tient à jour la synchronisation des données avec Project Server.
    
- (D) lorsqu’un projet est publié dans Project Professionnel, l’utilisateur a la possibilité de créer un site de projet pour le projet. Un projet peut également être créé dans Project Web App comme un type de projet de liste de tâches SharePoint ou comme un type de projet d’entreprise avec contrôle total (TPE). Étape (D) affiche le TPE de contrôle total.
    
**Figure 1. Utilisation des sites de projet en tant que listes des tâches SharePoint**

![Utilisation de sites de projet en mode visibilité] (media/pj15_Architecture_VisibilityMode.gif "Utilisation de sites de projet en mode visibilité")

<br/>

### <a name="managing-projects-with-full-control"></a>Gestion de projets avec contrôle total
<a name="pj15_Architecture_ManagedMode"> </a>

Lorsque Project Server est associé à une collection de sites et possède un contrôle total, Project Server importe les listes des tâches en tant que projets d’entreprise de SharePoint et peut supprimer tous les fichiers .mpp connexes. Project Server tient à jour les données de base pour la synchronisation des tâches ; listes de tâches dans la collection de sites sont en lecture seule (voir Figure 2). Les projets importés peuvent être modifiés à l’aide de Project Professionnel ou à l’aide de Project Web App.
  
> [!NOTE]
> Une fois que Project Server a importé un projet, l’utilisateur indique s’il veut supprimer le projet du site ou annuler la connexion avant la modification du projet. Vous pouvez effectuer la sélection dans Project Professionnel. 
  
La figure 2 illustre les processus suivants lorsque Project Server tient à jour les projets d’entreprise avec un contrôle total :
  
- (A) L’utilisateur peut choisir les sites de projet à importer. Project Server importe les sites de projet et supprime éventuellement les fichiers .mpp associés. La liste des tâches SharePoint d’un projet importé passe en lecture seule.
    
- (B) après l’association, Project Professional crée de nouveaux projets et enregistre ou publie dans Project Server. Le Cache actif dans Project Professionnel gère la synchronisation des données avec Project Server. Le composant WebPart de planification dans Project Web App peut faire planification côté serveur.
    
- (C) lorsqu’un projet est publié dans Project Professionnel, l’utilisateur a la possibilité de créer un site de projet pour le projet. Un projet peut également être créé dans Project Web App avec un TPE contrôle total et publié avec une liste de tâches en lecture seule pour un site de projet dans la collection de sites.
    
**Figure 2. Utilisation de sites de projet avec un contrôle total**

![Utilisation de sites de projet en mode géré] (media/pj15_Architecture_ManagedMode.gif "Utilisation de sites de projet en mode géré")
  
## <a name="general-architecture"></a>Architecture générale
<a name="pj15_Architecture_General"> </a>

La figure 3 montre une vue générale de l’architecture de Project Server 2013, y compris l’Application de Service Project, une seule instance de Project Web App sur un serveur Web frontal et plusieurs autres applications clientes, y compris Project Professional 2013.
  
Il peut y avoir plusieurs instances de Project Web App qui communiquent avec l’Application de Service de projet principal. Pour une installation locale, le serveur Web frontal peut se trouver sur un serveur distinct dans une batterie de serveurs SharePoint, ou il peut être sur le même serveur SharePoint avec l’Application de Service Project. Project Online comprend un serveur Web frontal, Application de Service Project et un serveur de Workflow Manager Client 1.0 local ou distant. 
  
**Figure 3. Architecture générale de Project Server 2013**

![Architecture de Project Server] (media/pj15_Architecture_ProjectServiceApp_WFE.gif "Architecture de Project Server")

<br/>

Les commentaires généraux suivants s’appliquent à la figure 3 :
  
- **Project Online :** Vous pouvez créer des applications qui utilisent les interfaces CSOM, REST et OData. Un package d’application peut également installer des récepteurs d’événements distants dans un service web personnalisé sur un serveur local, sur un serveur Azure ou sur Microsoft Azure. Project Online ne prend pas en charge tiers solutions locales, l’interface WCF, l’interface ASMX ou les gestionnaires d’événements locaux. 
    
- **Récepteurs d’événements :** Récepteurs d’événements peuvent également être appelées gestionnaires d’événements. Project Online prend en charge l’inscription à distance Project Server de récepteurs d’événements, qui peut être utilisé par une instance de Project Web App dans le nuage ou par une installation de Project Server sur site. Une installation de Project Server local prend en charge les récepteurs d’événements distants et les gestionnaires d’événements locaux de confiance totale. 
    
- **Navigateurs :** Il n’existe aucune limitation élargie des navigateurs sur l’affichage de certaines pages de Project Web App, qu’il existe dans Project Server 2010. Les navigateurs suivants sont pris en charge pour une utilisation complète avec Project Web App : 
    
  - Internet Explorer 8.x (sur Windows 7 et versions antérieures de Microsoft Windows), Internet Explorer 9.x et Internet Explorer 10.x 
  - Firefox 4.x (sur Windows, Mac OS-X et Linux/Unix)
  - Safari 5.x (sur Windows et Mac OS-X)
  - Chrome
    
- **Interfaces de programmation :** Pour les applications tierces, Project Online expose l’interface HTTP/HTTPS (y compris le reste), l’interface CSOM, un service OData pour CSOM et un service OData pour les rapports. Pour les applications de client tiers qui sont en local (sur l’Intranet), vous pouvez utiliser l’interface WCF pour l’interface PSI, ou vous pouvez utiliser les interfaces CSOM, OData et REST par le biais de HTTP. Les clients Project Web App et Project Professional 2013 utilisent l’interface WCF. Dans une installation de serveur unique, les services web, CSOM et REST ASMX frontal en interne appellent les services WCF principale. 
    
    > [!NOTE]
    > L’interface ASMX basés sur SOAP pour les services web dans PSI est toujours disponible dans Project Server 2013, mais il est déconseillé. 
  
    Le service OData pour les rapports est implémenté par le service WCF OData.svc interne. Vous pouvez obtenir le Document de métadonnées de Service pour les données de création de rapports à l’aide de `https://ServerName/ProjectServerName/_api/ProjectData/$metadata`. 
    
    Le service OData pour CSOM est destiné aux plateformes telles que Windows RT, iOS et Android, où vous pouvez utiliser l’interface REST avec JavaScript dans les pages HTML. 
    
    > [!NOTE]
    > Bien que le `$metadata` option pour la **ProjectData** reporting service n’est valide, la `$metadata` option pour le service **ProjectServer** de CSOM est supprimé dans la version de Project Server 2013. Pour plus d’informations sur les requêtes REST pour le modèle CSOM, voir [modèle d’objet côté Client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md). 
  
- **PSI redirecteur :** L’accès par programme à l’interface PSI sur un serveur Web frontal distinct passe par le redirecteur PSI, qui inclut un redirecteur WCF et un redirecteur de Service Web. Les clients qui utilisent l’interface ASMX accèdent à l’interface PSI par le biais du redirecteur de Service Web. Les clients qui utilisent l’interface WCF accèdent à l’interface PSI par le biais du redirecteur WCF. Accès par programme via le modèle CSOM, OData et REST est redirigée par le biais du redirecteur WCF. 
    
- **Flux de travail :** Flux de travail déclaratifs (flux de travail qui est définis dans SharePoint Designer 2013) est déchargé à Workflow Manager Client 1.0 pour le traitement. Workflow Manager Client 1.0 peut s’exécuter sur un serveur distinct dans la batterie de serveurs SharePoint, sur Microsoft Azure dans le nuage ou sur un seul ordinateur Project Server pour le test ou des démonstrations. Flux de travail codés développées avec Visual Studio 2012 est traités dans le module d’exécution du flux de travail dans SharePoint, comme dans Project Server 2010. Pour plus d’informations, voir [mise en route du développement de flux de travail Project Server](getting-started-developing-project-server-workflows.md).
    
- **Réseau de périmètre (DMZ) :** La figure 3 n’affiche pas qu’un serveur Web frontal de locale peut être isolé par un pare-feu supplémentaire dans un réseau de périmètre (également appelé « zone démilitarisée » ou DMZ). Un réseau de périmètre permettre permettre aux clients Internet d’accéder à SharePoint et Project Server à travers un pare-feu. 
    
- **Des Services Web SharePoint :** La figure 3 n’affiche pas l’infrastructure SharePoint, telles que l’application de Services Web SharePoint principale, qui fait partie de SharePoint Server 2013. Lorsque vous installez Project Server, l’Application de Service Project est ajoutée aux Services Web SharePoint. 
    
Le niveau frontal inclut les applications tierces, Project Professionnel et Project Web App. Un navigateur affiche les pages ASP.NET 4.0 (pages .aspx) dans Project Web App. Les pages de Project Web App utilisent les composants WebPart Project Server qui communiquent avec l’interface PSI et également utiliser des composants WebPart SharePoint standard. 
  
La couche intermédiaire inclut la PSI et la couche des objets métiers, qui se compose d’objets logiques qui représentent des entités d’entreprise Project Server. Les entités métier incluent le projet, tâche, ressource, affectation et ainsi de suite. L’interface PSI et le niveau d’objet métier sont étroitement et se trouvent sur le même serveur. Une application cliente appelle la PSI par le biais d’une des interfaces disponibles et la PSI appelle les objets métier. Pour améliorer les performances, le serveur Web frontal de Project Server 2013 inclut certains objets d’entreprise pour les demandes qui ne pas utiliser le système de mise en attente de Project Server ou nécessitent le Service de calcul Project. Les objets Web frontaux communiquent directement avec la base de données de projet.
  
Les composants de Project Web App de Project Server utilisent la base de données de configuration de SharePoint 2013 pour la configuration du site de projet et la base de données de contenu pour le contenu de site de projet tels que des listes de tâches, pages personnalisées, flux de travail, les paramètres de gestion, les documents et les listes de problèmes, risques et engagements. La configuration de SharePoint et les bases de données prise en charge des fonctionnalités supplémentaires pour la gestion de projet, telles que les modèles de projet et les espaces de travail, les listes personnalisées pour la collaboration d’équipe et des rapports.
  
### <a name="project-web-app-and-the-wfe"></a>Project Web App et composant web frontal
<a name="pj15_Architecture_PWAServer"> </a>

Vous pouvez configurer plusieurs instances de Project Web App sur un serveur Web frontal et plusieurs serveurs Web frontaux au sein d’un intranet d’entreprise pour activer la distribution de charge pour les clients de l’intranet. Lorsqu’une application cliente utilise une instance Project Web App sur un serveur Web frontal distinct, les appels PSI sont acheminées via le redirecteur PSI. Le redirecteur PSI (redirecteur WCF ou du redirecteur de Service Web) effectue les fonctions suivantes :
  
- Optimise les appels à PSI à partir de clients distants.
    
- Fait la différence entre les appels PSI qui nécessitent ou non le service de file d’attente Project Server. Les noms de méthodes PSI asynchrones commencent par Queue, par exemple **QueueCreateProject**.
    
- Identifie les appels PSI qui appellent des gestionnaires d’événements locaux enregistrés.
    
- Identifie les appels PSI qui nécessitent le service de calcul Project.
    
- Utilise un cache basé sur un serveur qui fonctionne avec le cache actif côté client dans Project Professionnel pour réduire le nombre d’appels en boucle à Project Server.
    
Une fois que SharePoint Server authentifie un utilisateur Project Server, le redirecteur PSI en toute transparence envoie des requêtes qui utilisent les services de serveur principal pour les services PSI sur l’ordinateur qui exécute Project Server. Requêtes qui ne nécessitent pas les services principaux sont envoyées aux objets métier dans l’instance de Project Web App locale. Le redirecteur PSI améliore l’évolutivité, de performances et la fiabilité pour Project Server de traitement sur le réseau local, un réseau étendu et dans Project Online.
  
Project Web App est développée avec ASP.NET 4.0. Les éléments visuels dans les fichiers .aspx (HTML, contrôles serveur et texte statique) sont distincts de la logique de programmation dans les classes code-behind qui se trouvent dans des assemblys compilés (fichiers .dll). Pages de site dans Project Web App, telles que la page de niveau supérieur, le centre de projets et le centre de rapports, peuvent être personnalisés à l’aide de composants WebPart. Impossible de modifier les pages d’application qui n’ont pas une option de **Modifier la Page** dans le menu **Actions du Site** , telles que la page Paramètres du serveur et de la page de feuille de temps de révision. 
  
### <a name="the-csom-and-the-project-server-interface"></a>CSOM et PSI (Project Server Interface)
<a name="pj15_Architecture_PSI"> </a>

L’interface PSI est pris en compte dans 22 services publics, tels que le **projet**, **ressource**, **CustomField**et **état**. L’interface PSI contient également des sept services privés à un usage interne. L’interface PSI est l’API fondamentales de Project Server ; Il expose les fonctionnalités de Project Server CSOM et des applications externes. Le modèle CSOM inclut les classes qui accèdent les plus couramment utilisées PSI classes et membres qui sont utilisés pour les applications tierces. Dans Project Server 2013, certaines fonctionnalités de Project Server ne sont pas disponible dans le modèle CSOM, tels que les services **d’administration**, **calendrier**, **PortfolioAnalyses**et la **sécurité** . 
  
Project Professional 2013 et l’utilisation de Project Web App pour accéder aux données de Project Server dans le brouillon, publiée, l’interface PSI et archiver des tables et les vues de la base de données de projet. Vous pouvez accéder à un service PSI via un fichier proxy ou un assembly de proxy pour les services WCF ou les services web ASMX.
  
> [!NOTE]
> Le modèle CSOM est l’interface par défaut pour les développeurs Project Server de tiers ; Il peut être utilisé pour les applications qui accèdent à une installation de Project Server sur site et de Project Online. Nous vous recommandons d’utiliser le modèle CSOM pour le développement de nouvelles applications, si le modèle inclut les fonctionnalités dont votre application a besoin. 
  
Certains line-of-business applications métier et autres applications de tiers qui ont été développées pour Project Server 2010 requièrent les services PSI qui ne figurent pas encore dans le modèle CSOM. Si elles ciblent uniquement une installation locale de Project Server, les applications peuvent continuer à utiliser l’interface WCF ou ASMX de la PSI.
  
Applications clientes appellent PSI par le biais de proxys de service. Tous les services PSI par le biais d’accéder aux clients qui utilisent l’interface WCF `https://ServerName/ProjectServerName/_vti_bin/psi/ProjectServer.svc`. Les clients qui utilisent une interface de service web ASMX utilisent l’URL Project Web App pour le service spécifique. Par exemple, le service de **ressources** est à `https://ServerName/ProjectServerName/_vti_bin/psi/resource.asmx?wsdl`. Si les applications n’ont pas accès intranet à Project Server, ils peuvent utiliser un serveur de Project Web App dans un réseau de périmètre (non illustré à la Figure 3).
  
La figure 4 illustre le volet **connexions** dans le **Gestionnaire des Services Internet (IIS)** pour une installation de serveur unique d’un site local de la gestion des flux de travail SharePoint Server 2013 et Project Server 2013 pour Workflow Manager Client 1.0. La collection de sites SharePoint (A) inclut les services frontaux PSI dans le `_vti_bin\PSI` sous-répertoire virtuel. L’application de Services Web SharePoint (B) inclut l’Application de Service Project, avec les services PSI principal dans le `508c23fb7dfd4c83a8919fae24bc68c5/PSI` sous-répertoire virtuel. Le GUID est le nom de l’instance de l’Application de Service Project pour cette installation de Project Server. 
  
**Figure 4. Gestionnaire IIS affichant le service PSI frontal (A) et le service PSI principal (B)**

![PSI frontal et PSI dorsal] (media/pj15_Architecture_PSI_IIS.gif "PSI frontal et PSI dorsal")
  
Applications clientes ne peut pas accéder directement les services WCF pour l’interface PSI dans l’Application de Service de projet principal. Si elles ne nécessitent pas d’accès à Project Online, les applications clientes et composants d’applications cœur de métier utilisent le proxy pour l’interface PSI. Une URL principale pour le service de **ressources** dans la Figure 4, par exemple, l’interface WCF serait `https://ServerName:32843/508c23fb7dfd4c83a8919fae24bc68c5/psi/resource.svc`. Port 32843 est le port HTTP par défaut pour l’application de Services Web SharePoint (32844 est le port pour les communications HTTPS). Toutefois, le fichier web.config de blocs de Project Web App un accès direct aux services PSI principal.
  
> [!NOTE]
> Le téléchargement du Kit de développement Project 2013 inclut des fichiers proxy PSI pour les services WCF et ASMX et comment les compiler dans des assemblys de proxy. > Pour créer des fichiers proxy PSI mis à jour qui utilisent l’interface WCF, vous devez utiliser l’utilitaire svcutil.exe ou dans Visual Studio directement sur l’ordinateur Project Server. 
  
Généralement, les membres des services PSI produisent ou consomment des objets **DataSet** typés comme moyen d’échanger des informations avec les objets métier. Il existe également plusieurs modèles différents pour le développement de la PSI. Par exemple, les services PSI **LookupTable** , **CustomFields**et **ressources**utilisent des objets filtre XML pour la manipulation du **jeu de données** , et autres services pas ; certaines méthodes dans le service **d’état** utilisent un paramètre _changeXml_ , tandis que d’autres méthodes et services ne mais pas. Le modèle CSOM n’utilise pas de jeux de données. Bien que le modèle CSOM possède un modèle de programmation différent de la PSI, et vous pouvez utiliser des assemblys .NET ou JavaScript, développement avec le modèle CSOM est généralement plus simple et plus cohérente que le développement avec la PSI. 
  
Pour plus d’informations sur l’interface PSI, voir [vue d’ensemble de la référence PSI Project](project-psi-reference-overview.md). Pour plus d’informations sur le modèle CSOM, voir [modèle d’objet côté Client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="business-objects-in-the-wfe-and-the-project-service-application"></a>Objets métier du composant web frontal et application de service Project
<a name="pj15_Architecture_BusinessObjects"> </a>

Le modèle objet interne de Project Server inclut des objets métier, qui représentent des entités logiques telles que des projets et des ressources. Les applications clientes accèdent aux objets métier uniquement par le biais de CSOM ou PSI. Les objets métier quant à eux accèdent aux ébauches de tables et d’affichages, et aux tables et affichages publiés et archivés dans la base de données Project.
  
Les objets métier ne sont pas exposés aux développeurs tiers. PSI gère le mappage de l’API aux objets métier, et CSOM mappe son API à PSI. Les entités logiques d’objets métier peuvent être classées en trois catégories :
  
- Les **entités de base** sont des objets tels que des projets, tâches, attributions, ressources et calendriers. Elles incluent la logique métier de base, comme les autorisations et les règles d’attribution de noms. 
    
- Les **entités métier** sont des objets tels que des feuilles de temps, portefeuilles de projets et modèles. Elles incluent une logique métier supplémentaire et sont généralement basées sur une combinaison d’entités de base. 
    
- Les **entités de prise en charge** sont des objets, tels que la sécurité et la validation. 
    
Dans Project Server 2010, tous les objets métier sont implémentées dans l’Application de Service Project. Dans Project Server 2013, le serveur Web frontal héberge bon nombre d’objets métiers traitent des méthodes synchrones et ne nécessitent pas le Service de calcul Project. Méthodes PSI synchrones telles que **DeleteProject** et **ReadAssignments** n’utilisent pas le Service de file d’attente de Project Server. Les méthodes asynchrones dans l’interface PSI portent des noms qui commencent par `Queue`, telles que **QueueCreateProject** et **QueueUpdateTimesheet**. Une méthode asynchrone envoie un message pour le Service de file d’attente de Project Server, qui planifie le traitement de la méthode pendant que le contrôle est renvoyé à l’utilisateur.
  
Le redirecteur PSI détermine les requêtes qui sont envoyées à l’application de service Project et qui peuvent être traitées par les objets métier dans le composant web frontal. Les objets métier du composant web frontal ignorent l’application de service Project et ont un accès direct à la base de données Project, tout comme les autres processus SharePoint du composant web frontal accèdent directement aux bases de données de configuration et de contenu. L’exécution de nombreux objets métier du composant web frontal améliore l’efficacité de Project Server, réduit la charge sur le niveau de l’application et permet à Project Server une meilleure mise à l’échelle pour les charges de travail accrues.
  
> [!NOTE]
> Dans Project Server 2013, les gestionnaires d’événements locaux doivent être déployés pour le serveur Web frontal et l’ordinateur de Project Server principale. 
  
### <a name="project-server-database"></a>Base de données Project Server
<a name="pj15_Architecture_DAL"> </a>

Dans Project Server 2013, les quatre bases de données Project Server des versions précédentes sont regroupés dans une base de données Project dans SQL Server. Le nom de base de données de projet par défaut est ProjectService. Les tables et les affichages de rapports conservent leur nom précédente avec la `dbo` préfixe, tel que dbo. MSP_EpmProject et dbo. MSP_EpmProject_UserView. Tables et les vues qui ont été précédemment dans la base de données provisoire ont le `draft` préfixe. Tables et vues à partir de la base de données publiée ont le `pub` préfixe. Tables et vues à partir de la base de données Archive ont le `ver` préfixe. 
  
> [!IMPORTANT]
> Direct access n’est pas pris en charge pour le brouillon ( `draft` préfixe), publié ( `pub` préfixe) et d’archivage ( `ver` préfixe) tables et les vues. Rapports doivent utiliser uniquement les tables et vues, dont la création de rapports le `dbo` préfixe. 
  
Les données Project Server sont partitionnées dans la base de données Project comme suit :
  
- Brouillon tables et vues contiennent des données à partir de projets non publiés qui ont été créées par Project Professionnel et d’autres applications. Project Web App n’affiche pas les données de projet dans les vues et tables de brouillon.
    
- Les tables publiées et les vues contiennent tous les projets publiés et les ressources d’entreprise, les données globales pour les types de projets d’entreprise (TPE) et autres modèles de projet. Projets publiés sont visibles dans Project Web App. Les données publiées incluent également des tables qui sont spécifiques à Project Web App (feuilles de temps, modèles, vues, etc.) et les tables de données globales (champs personnalisés, tables de choix, les autorisations Project Server et métadonnées).
    
- Les données d’archive enregistrent des versions de sauvegarde des projets, des ressources, des champs personnalisés et d’autres données.
    
- Les données de création de rapports peuvent être utilisées pour l’accès en lecture seule dans les applications tierces et pour les rapports. Les cubes OLAP Server Project utilisent les affichages de rapports dont le `_OlapView` suffixe. Les cubes OLAP sont disponibles dans une installation de Project Server locaux, mais ne sont pas disponibles dans Project Online. 
    
    Les données de génération de rapports sont complètes et mises à jour presque en temps réel. Les tables et affichages de génération de rapports sont optimisés pour la génération de rapports en lecture seule ; par exemple, les tables de génération de rapports sont dénormalisées pour fournir des données redondantes et réduire le nombre de tables relationnelles.
    
Les entités logiques telles que les ressources et les projets peuvent être situées dans plusieurs tables, et toutes les tables d’une entité spécifique ont la même clé principale. Cette dernière correspond au GUID d’une colonne unique qui identifie de manière unique une instance spécifique d’une entité donnée.
  
Données Project Server pour chaque instance de Project Web App sont stockées dans une base de données de projet séparé avec un nom différent. Les applications clientes qui ont un accès direct à Project Server peuvent lire directement les tables et les affichages de rapports. Pour l’accès distant, applications clientes peuvent utiliser l’interface OData et l’interface REST pour obtenir des données pour les rapports. Les clients doivent utiliser uniquement le modèle CSOM ou la PSI pour accéder le brouillon, publiée et archiver des tables et les vues. Le Service de données de création de rapports (RDS, qui n’est pas affiché dans la Figure 3) met à jour les données de création de rapports à partir des données publiées dans presque en temps réel. La base de données de projet peut se trouver sur un serveur distinct.
  
Schémas sont documentées uniquement pour les tables et les affichages de rapports. Pour une installation de Project Server sur site, vous pouvez ajouter des tables de rapports et des affichages pour les entités qui ne sont pas définis dans le schéma de base de données de projet. Vous pouvez également créer des bases de données distinctes pour les applications personnalisées sur site. Modification n’est pas pris en charge pour le brouillon, publié et archive des tables et les vues. Étant donné que la base de données de projet n’est pas directement accessible dans Project Online, création de rapports tables et affichages ne sont pas modifiables. Toutefois, si vous disposez d’un compte SQL Azure, vous pouvez créer des bases de données distinctes pour une utilisation personnalisée avec Project Online.
  
### <a name="event-receivers"></a>Récepteurs d’événements
<a name="pj15_Architecture_EventHandlers"> </a>

Gestionnaires d’événements locaux et des récepteurs d’événements distants pour Project Server Activez extensibilité tiers en réponse aux événements Project Server tels que la création ou la publication d’un projet. Dans Project Server 2010, tous les gestionnaires d’événements locaux et sont écrites dans le code de confiance totale, déployé directement sur l’ordinateur qui exécute Project Server et pour le Web frontaux et s’exécutent dans le système d’événements Project Server. Étant donné que Project Online ne peuvent pas utiliser des gestionnaires d’événements de confiance totale, Project Server 2013 implémente des récepteurs d’événements distants qui sont similaires pour les récepteurs d’événements distants dans SharePoint Server 2013. Une installation locale de Project Server 2013 peut utiliser des gestionnaires d’événements de confiance totale traditionnel et des récepteurs d’événements distants.
  
Un récepteur d’événements distants Project Server peut être implémenté dans un service web personnalisé avec un point de terminaison SOAP qui s’exécute dans Microsoft Azure ou d’autres environnements qui prennent en charge des services web SOAP. Un package d’application Project Server peut inclure des récepteurs d’événements distants qui sont installés avec l’application.
  
Récepteurs d’événements distants peuvent rappeler dans Project Server à l’aide de points de terminaison CSOM (ne pas illustrés à la Figure 3). L’appel vers un récepteur d’événements distants consacrée des informations depuis le système d’événements Project Server et l’instance Project Web App (ou le client Project Web App dans Project Online) qui émet l’appel. Récepteurs d’événements distants permettent de créer et héberger un service web unique qui peut être utilisé par plusieurs installations de Project Server. En revanche, les gestionnaires d’événements locaux de confiance totale doivent être déployés sur chaque installation de Project Server.
  
### <a name="publishing-and-server-side-scheduling"></a>Publication et planification côté serveur
<a name="pj15_Architecture_PublishingScheduling"> </a>

Project Server 2013 prend en charge les mises à jour de la planification manuelle et automatisée du projet. Le processus par défaut est une mise à jour de la planification manuelle. Autrement dit, le responsable de projet extrait et ouvre un projet dans Project Professionnel ou Project Web App, applique les modifications, puis enregistre et publie le projet pour apporter les modifications disponibles pour tout le monde. Project Professionnel possède un moteur de planification calcule les modifications, puis enregistre les modifications apportées à Project Server. Dans Project Server 2010, le moteur de planification côté serveur est une implémentation différente du moteur de planification dans Project Professionnel.
  
Dans Project Server 2013, le Service de calcul Project implémente le même moteur de planification dans Project Professional 2013. Le Service de calcul Project s’exécute dans un service Windows nommé **Service de calcul de Microsoft Project Server**. Modification d’une planification de projet dans Project Web App ou avec des applications tierces qui utilisent les résultats CSOM dans exactement les mêmes modifications planification que Project Professionnel.
  
> [!NOTE]
> Les applications tierces qui utilisent la PSI peuvent afficher des différences de planification à partir d’une planification calcule Project Web App. Pour la compatibilité descendante, les méthodes PSI publics que côté serveur planification toujours utilisent le moteur de planification qui a été introduit dans Project Server 2010. Une exception est **QueueUpdateProject2**, qui est une nouvelle méthode PSI dans Project Server 2013. Par exemple, le moteur de planification plus ancien ne planifie pas sous-projets ou des liens vers d’autres projets et ne calcule pas les champs de la valeur acquise. Pour éviter les potentiels de planification des différences entre les applications tierces et Project Professional ou Project Web App, vous devez développer d’applications avec le modèle CSOM lorsque cela est possible. 
  
Pour autoriser la mise à jour de la version publiée d’un projet alors qu’un responsable de projet utilise une ébauche de version, Project Server procède comme suit :
  
1. Project Server applique les mises à jour et replanifie la version publiée.
    
2. Project Server enregistre la mise à jour à appliquer à l’ébauche de version lorsque l’un des événements suivants se produit :
    
   - Project Professionnel ouvre le projet.
    
   - Project Professional tente de publier le projet.
    
3. En cas de conflit, le responsable du projet en est informé et doit résoudre le conflit avant la publication de l’ébauche de version.
    
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de Project 2013 pour les développeurs](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)
- [Programmabilité de Project Server](project-server-programmability.md)  
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)  
- [Fonctionnalités de l’interface PSI](what-the-psi-does-and-does-not-do.md)  
- [Prise en main du développement de flux de travail Project Server](getting-started-developing-project-server-workflows.md)   
- [Présentation des références de projet PSI](project-psi-reference-overview.md)   
- [Protocole Open Data](https://www.odata.org/)
    

