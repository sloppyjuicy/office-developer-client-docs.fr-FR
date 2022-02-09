---
title: Architecture Project Server
manager: soliver
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 2cfa5a6e-2f5c-440c-b35a-bc7a34648f9c
description: Project Server 2013 intègre des fonctionnalités de gestion de projet dans une batterie de serveurs SharePoint et autorise l’utilisation de Project Online avec un modèle objet client (CSOM) et une interface OData pour les données de création de rapports.
ms.localizationpriority: high
ms.openlocfilehash: 258a269176d286edb23a9749626038bb48ab48e4
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462791"
---
# <a name="project-server-architecture"></a>Architecture Project Server

Project Server 2013 intègre des fonctionnalités de gestion de projet dans une batterie de serveurs SharePoint et autorise l’utilisation de Project Online avec un modèle objet client (CSOM) et une interface OData pour les données de création de rapports.
   
Project Server 2013 est un système multicouche qui étend l’architecture introduite dans Office Project Server 2007. Les modifications apportées à l’architecture incluent l’association du service d’application Project avec les collections de sites SharePoint, l’ajout de certains objets métier dans le composant web frontal (WFE), le modèle objet client (CSOM) pour l’accès distant, une unique base de données Project, une interface OData pour les tables et affichages de la création de rapports, l’intégration de Windows Workflow Foundation version 4 (WF4) via Workflow Manager Client 1.0 dans le cloud ou sur un serveur local et les récepteurs d’événements distants accessibles par plusieurs installations Project Server. En plus des solutions personnalisées en local, vous pouvez créer des applications qui incluent des récepteurs d’événements à distance et des composants qui accèdent aux interfaces CSOM et OData.
  
La couche frontale comprend Project Professionnel 2013, Project Web App, et des applications tierces. Les applications clientes communiquent avec la couche intermédiaire par le biais de l’interface Project Server ou de points de terminaison du modèle objet côté client, qui à leur tour communiquent avec l’interface Project Server et la couche d’objets métier. L’accès aux bases de données est intégré aux objets métier. Le système d’événements Project Server peut accéder aux gestionnaires d’événements locaux et aux récepteurs d’événements distants. Le Service de calcul de Project implémente le moteur de planification Project Professionnel dans Project Server. Les applications clients n’accèdent pas (et ne doivent pas accéder) directement à la base de données Project ; Project Server masque les objets métier aux yeux des clients.
  
> [!NOTE]
> Project Server est basé sur l’architecture SharePoint. Pour plus d’informations sur l’architecture SharePoint Server 2013 et le modèle d’application SharePoint, consultez la section relative à la *prise en main du développement SharePoint* de la documentation Office 2013 destinée aux développeurs. 

<a name="pj15_Architecture_SharePoint"> </a>

## <a name="integrating-with-sharepoint-site-collections"></a>Intégration aux collections de sites SharePoint

Le Service d’application Project dans Project Server 2013 peut être associé à une collection de sites SharePoint pour une utilisation avec des listes de tâches SharePoint. Le Service d’application Project peut également importer une liste de tâches SharePoint en tant que projet d’entreprise pour un contrôle Project Server total. Avec une liste de tâches SharePoint, SharePoint tient à jour le site de projet dans une collection de sites ; Project Professionnel peut synchroniser et mettre à jour la liste des tâches. Un site de projet peut être une liste de tâches SharePoint indépendante ou une liste de tâches synchronisée avec un fichier .mpp ; le fichier .mpp peut être stocké localement ou dans une bibliothèque SharePoint. 
  
Project Server tient à jour les projets lorsqu’il a un contrôle total ; Project Professionnel enregistre les données directement dans Project Server. Le tableau 1 compare le comportement d’une liste de tâches, le composant WebPart Planification et d’autres fonctionnalités pour le contrôle SharePoint des listes de tâches et pour les projets importés lorsque Project Server a un contrôle total. Le composant WebPart Planification contient la grille dans la page Project Web App où vous pouvez modifier une planification de projet. En mode lié, les données de gestion des états sont saisies une fois pour les tâches et les feuilles de temps ; en mode d’entrée unique, les données de gestion des états de la tâche sont saisies séparément des feuilles de temps.
  
**Tableau 1. Comparaison des listes de tâches SharePoint et contrôle total**

| Fonctionnalité | Liste des tâches | Contrôle total |
|:-----|:-----|:-----|
|**Liste de tâches dans SharePoint** <br/> |Lecture/écriture  <br/> |Lecture seule  <br/> |
|**Composant WebPart Planification** <br/> |Lecture seule  <br/> |Lecture/écriture  <br/> |
|**Rapports** <br/> |Création de rapports enrichis par le biais de Project Server  <br/> |Création de rapports enrichis par le biais de Project Server  <br/> |
|**Autres fonctionnalités de Project Server** <br/> | Fonctionnalité bloquée :  <br/>- Modifications de projets côté serveur, avec Project Web App ou des applications clientes personnalisées  <br/>- Gestion des états  <br/>- Les tâches ne sont pas visibles en mode lié  <br/> |Les fonctionnalités complètes sont activées  <br/> |
   
### <a name="managing-projects-as-sharepoint-task-lists"></a>Gestion de projets en tant que listes de tâches SharePoint
<a name="pj15_Architecture_VisibilityMode"> </a>

Lorsque Project Server est associé à une collection de sites SharePoint dans laquelle SharePoint tient à jour le contrôle, les listes de tâches et les fichiers Project Professionnel 2013 (.mpp) dans les bibliothèques de documents sont visibles par le Service d’application Project, mais SharePoint tient à jour les données principales pour la synchronisation (voir Figure 1). La planification côté serveur avec le composant WebPart Planification ne peut pas être effectuée. Vous pouvez utiliser Project Professionnel pour synchroniser et modifier la liste des tâches dans un site de projet. En commençant par les listes de tâches SharePoint, les organisations peuvent progressivement évoluer pour utiliser toutes les fonctionnalités de Project Server.
  
La figure 1 indique les processus suivants lorsque les projets sont tenus à jour dans des listes de tâches SharePoint : 
  
- (A) Project Professionnel peut synchroniser la liste des tâches et créer des sites de projet dans la collection de sites avant ou après l’association avec le service d’application Project.
    
- (B) Project Server synchronise les données du site de projet à des fins de génération de rapports, mais SharePoint tient à jour les données de base ; les listes des tâches restent en lecture/écriture.
    
- (C) Après l’association, Project Professionnel peut créer des projets et les enregistrer ou les publier dans Project Server. Le cache actif dans Project Professionnel tient à jour la synchronisation des données avec Project Server.
    
- (D) Lorsqu’un nouveau projet est publié dans Project Professionnel, l’utilisateur peut créer un site de projet pour le projet. Un projet peut également être créé dans Project Web App comme type de projet de liste de tâches SharePoint ou comme type de projet d’entreprise avec contrôle total. L’étape (D) présente le type de projet d’entreprise avec contrôle total.
    
**Figure 1. Utilisation de sites de projet en tant que listes de tâches SharePoint**

![Utilisation de sites de projet en mode Visibilité](media/pj15_Architecture_VisibilityMode.gif "Utilisation de sites de projet en mode Visibilité")


### <a name="managing-projects-with-full-control"></a>Gestion de projets avec contrôle total
<a name="pj15_Architecture_ManagedMode"> </a>

Lorsque Project Server est associé à une collection de sites et a un contrôle total, Project Server importe les listes de tâches SharePoint en tant que projets d’entreprise et peut supprimer les fichiers .mpp connexes. Project Server tient à jour les données principales pour la synchronisation de la liste de tâches ; les listes de tâches dans la collection de sites deviennent accessibles en lecture seule (voir Figure 2). Les projets importés peuvent être modifiés à l’aide de Project Professionnel ou Project Web App.
  
> [!NOTE]
> Une fois que Project Server a importé un projet, l’utilisateur indique s’il veut supprimer le projet du site ou annuler la connexion avant la modification du projet. Vous pouvez effectuer la sélection dans Project Professionnel. 
  
La figure 2 illustre les processus suivants lorsque Project Server tient à jour les projets d’entreprise avec un contrôle total :
  
- (A) L’utilisateur peut choisir les sites de projet à importer. Project Server importe les sites de projet et supprime éventuellement les fichiers .mpp associés. La liste des tâches SharePoint d’un projet importé passe en lecture seule.
    
- (B) Après l’association, Project Professionnel crée des projets et les enregistre ou les publie dans Project Server. Le cache actif dans Project Professionnel tient à jour la synchronisation des données avec Project Server. Le composant WebPart Planification dans Project Web App peut effectuer une planification côté serveur.
    
- (C) Lorsqu’un nouveau projet est publié dans Project Professionnel, l’utilisateur peut créer un site de projet pour le projet. Un projet peut également être créé dans Project Web App avec un type de projet d’entreprise de contrôle total et publié avec une liste de tâches en lecture seule dans un site de projet dans la collection de sites.
    
**Figure 2. Utilisation de sites de projet avec contrôle total**

![Utilisation de sites de projet en mode géré](media/pj15_Architecture_ManagedMode.gif "Utilisation de sites de projet en mode géré")
  
## <a name="general-architecture"></a>Architecture générale
<a name="pj15_Architecture_General"> </a>

La figure 3 montre une vue générale de l’architecture Project Server 2013, notamment l’application de service Project, une unique instance Project Web App sur un composant web frontal et plusieurs autres applications clientes, Project Professionnel 2013.
  
Il peut y avoir plusieurs instances Project Web App qui communiquent avec l’application de service Project principale. Pour une installation locale, le composant web frontal peut se trouver sur un serveur distinct dans une batterie de serveurs SharePoint, ou il peut être sur le même serveur SharePoint avec l’application de service Project. Project Online inclut un composant web frontal, l’application de service Project et un serveur Workflow Manager Client 1.0 local ou distant. 
  
**Figure 3. Architecture générale Project Server 2013**

![Architecture Project Server](media/pj15_Architecture_ProjectServiceApp_WFE.gif "Architecture Project Server")


Les commentaires généraux suivants s’appliquent à la figure 3 :
  
- **Project Online :** Vous pouvez créer des applications qui utilisent les interfaces CSOM, REST et OData. Un package d'application peut également installer des récepteurs d'événements à distance dans un service web personnalisé sur un serveur local, sur un serveur Azure ou sur Microsoft Azure. Project Online ne prend pas en charge les solutions tierces en local, l'interface WCF, l'interface ASMX ni les gestionnaires d'événements locaux. 
    
- **Récepteurs d'événements :** Les récepteurs d'événements peuvent également être appelés gestionnaires d'événements. Project Online prend en charge l'inscription à distance des récepteurs d'événements de Project Server, qui peuvent être utilisés par une instance Project Web App dans le cloud ou par une installation de Project Server en local. Une installation de Project Server en local prend en charge les récepteurs d'événements à distance et les gestionnaires d'événements de confiance totale en local. 
    
- **Navigateurs :** il n’existe aucune limitation de multinavigation lors de l’affichage de certaines pages Project Web App, mais il y en a dans Project Server 2010. Les navigateurs suivants sont pris en charge pour une utilisation complète avec Project Web App : 
    
  - Internet Explorer 8.x (sur Windows 7 et les versions antérieures de Microsoft Windows), Internet Explorer 9.x et Internet Explorer 10.x 
  - Firefox 4.x (sur Windows, Mac OS-X, et Linux/Unix)
  - Safari 5.x (sur Windows et Mac OS-X)
  - Chrome
    
- **Interfaces programmatiques :** pour des applications tierces, Project Online expose l’interface HTTP/HTTPS (y compris REST), l’interface CSOM, un service OData pour CSOM et un service OData pour la création de rapports. Pour les applications clientes tierces qui sont en local (sur l’intranet), vous pouvez utiliser l’interface WCF pour l’interface PSI ou vous pouvez utiliser les interfaces CSOM, OData et REST via HTTP. Les clients Project Web App et Project Professionnel 2013 utilisent l’interface WCF. Dans une installation à un seul serveur, les services web ASMX frontaux, CSOM et REST en interne appellent les services WCF principaux. 
    
    > [!NOTE]
    > L’interface ASMX SOAP pour les services web dans PSI est toujours disponible dans Project Server 2013, mais obsolète. 
  
    Le service OData pour la création de rapports est implémenté par le service WCF OData.svc interne. Vous pouvez obtenir le document de métadonnées du service pour les données de rapport à l'aide de  `https://ServerName/ProjectServerName/_api/ProjectData/$metadata`. 
    
    Le service OData pour CSOM est prévu pour les plateformes telles que Windows RT, iOS et Android, où vous pouvez utiliser l’interface REST avec JavaScript dans des pages HTML. 
    
    > [!NOTE]
    > Même si l’option `$metadata` pour le service de création de rapports **ProjectData** est valide, l’option `$metadata` pour le service **ProjectServer** du modèle CSOM est supprimée dans la version publiée de Project Server 2013. Pour plus d’informations sur les requêtes REST pour le modèle CSOM, consultez la rubrique [Modèle objet côté Client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md). 
  
- **Redirecteur PSI :** l’accès programmatique au PSI dans un serveur WFE distinct transite via le redirecteur PSI, qui inclut un redirecteur WCF et un redirecteur de service web. Les clients qui utilisent l’interface ASMX accèdent au PSI via le redirecteur de service web, et ceux qui utilisent l’interface WCF y accèdent via le redirecteur WCF. L’accès programmatique via CSOM, OData et REST est redirigé via le redirecteur WCF. 
    
- **Flux de travail :**  : les flux de travail déclaratifs (flux de travail définis dans SharePoint Designer 2013) sont déchargés vers Workflow Manager Client 1.0 à des fins de traitement. Workflow Manager Client 1.0 peut s’exécuter sur un serveur distinct dans la batterie SharePoint, sur Microsoft Azure dans le cloud ou sur un ordinateur Project Server unique à des fins de test ou de démonstration. Les flux de travail codés développés avec Visual Studio 2012 sont traités dans le runtime de flux de travail dans SharePoint, comme dans Project Server 2010. Pour plus d’informations, consultez la rubrique [Prise en main du développement de flux de travail Project Server](getting-started-developing-project-server-workflows.md).
    
- **Réseau de périmètre (DMZ) :** la figure 3 ne montre pas qu’un serveur WFE local peut être isolé par un pare-feu supplémentaire dans un réseau de périmètre (également appelé « zone démilitarisée » ou DMZ). Un réseau de périmètre peut autoriser les clients Internet à accéder à SharePoint et Project Server via un pare-feu. 
    
- **Services web SharePoint :** la figure 3 ne montre pas l’infrastructure de SharePoint, notamment l’application Services web SharePoint principale, qui fait partie de SharePoint Server 2013. Lorsque vous installez Project Server, l’application de service Project est ajoutée aux services web SharePoint. 
    
La couche frontale inclut des applications tierces, Project Professionnel et Project Web App. Un navigateur affiche les pages ASP.NET 4.0 (pages .aspx) dans Project Web App. Les pages Project Web App utilisent des composants WebPart Project Server qui communiquent avec l'interface PSI et utilisent également des composants WebPart SharePoint standard. 
  
Le niveau intermédiaire inclut l’interface PSI et la couche objet métier, qui est constituée d’objets logiques représentant les entités métier de Project Server. Les entités métier incluent Projet, Tâche, Ressource, Affectation, etc. L’interface PSI et le niveau de l’objet métier sont étroitement couplés et sont situés sur le même serveur. Une application cliente appelle l’interface PSI via l’une des interfaces disponibles et l’interface PSI appelle les objets métier. Pour améliorer les performances, le serveur web frontal de Project Server 2013 inclut des objets métier pour les requêtes qui n’utilisent pas le système de mise en file d’attente de Project Server ou exigent le Service de calcul de Project. Les objets métier du serveur Web frontal communiquent directement avec la base de données de Project.
  
Les composants Project Web App de Project Server utilisent la base de données de configuration SharePoint 2013 pour la configuration du site de projet et la base de données de contenu pour le contenu de site de projet comme les listes de tâches, pages personnalisées, flux de travail, paramètres de gestion, documents et listes de problèmes, risques et engagements. Les bases de données de contenu et la configuration de SharePoint prennent en charge des fonctionnalités supplémentaires pour la gestion de projet, telles que les modèles de projet et espaces de travail, les listes personnalisées pour la collaboration en équipe et les rapports.
  
### <a name="project-web-app-and-the-wfe"></a>Project Web App et le serveur web frontal
<a name="pj15_Architecture_PWAServer"> </a>

Vous pouvez configurer plusieurs instances de Project Web App sur un serveur web frontal et plusieurs serveurs web frontaux dans un intranet d’entreprise afin de permettre la distribution de charge pour les clients intranet. Lorsqu’une application cliente utilise une instance Project Web App sur un serveur web frontal distinct, les appels de l’interface PSI sont routés via le redirecteur PSI. Le redirecteur PSI (redirecteur WCF ou redirecteur de service web) effectue les fonctions suivantes :
  
- Optimise les appels à l’interface PSI à partir de clients distants.
    
- Fait la différence entre les appels PSI qui nécessitent ou non le service de file d’attente Project Server. Les noms de méthodes PSI asynchrones commencent par Queue, par exemple **QueueCreateProject**.
    
- Identifie les appels PSI qui appellent les gestionnaires d’événements locaux inscrits.
    
- Identifie les appels PSI qui nécessitent le service de calcul Project.
    
- Utilise un cache basé sur le serveur qui fonctionne avec le cache actif côté client dans Project Professionnel afin de réduire les appels en boucle à Project Server.
    
Une fois que SharePoint Server authentifie un utilisateur Project Server, le redirecteur PSI envoie en toute transparence des requêtes qui utilisent des services principaux aux services PSI sur l’ordinateur exécutant Project Server. Les requêtes qui ne nécessitent pas de services principaux sont envoyées aux objets métier dans l’instance Project Web App locale. Le redirecteur PSI améliore l’évolutivité, les performances et la fiabilité pour le traitement Project Server sur le LAN, un WAN et dans Project Online.
  
Project Web App est développé avec ASP.NET 4.0. Les éléments visuels dans les fichiers .aspx (HTML, contrôles serveur et texte statique) sont séparés de la logique programmatique dans les classes code-behind qui se trouvent dans des assemblys compilés (fichiers .dll). Les pages de site dans Project Web App, telles que la page de niveau supérieur, le centre de projets et le centre de rapports, peuvent être personnalisés à l’aide de composants WebPart. Les pages d’application qui n’ont pas une option **Modifier la page** dans le menu **Actions du site** ne peuvent pas être modifiées (la page Paramètres du serveur et la page Réviser la feuille de temps, par exemple). 
  
### <a name="the-csom-and-the-project-server-interface"></a>Le modèle CSOM et l’interface Project Server
<a name="pj15_Architecture_PSI"> </a>

L’interface PSI est prise en compte dans 22 services publics, tels que **Project**, **Resource**, **CustomField** et **Statusing**. L’interface PSI contient également sept services privés pour une utilisation interne. L’interface PSI est l’API fondamentales de Project Server ; elle expose les fonctionnalités de Project Server au modèle CSOM et aux applications externes. Le modèle CSOM inclut des classes qui accèdent aux membres et aux classes PSI les plus utilisés pour des applications tierces. Dans Project Server 2013, certaines fonctionnalités de Project Server ne sont pas disponibles dans le modèle CSOM, comme les services **Admin**, **Calendar**, **PortfolioAnalyses** et **Security**. 
  
Project Professionnel 2013 et Project Web App utilisent l’interface PSI pour accéder aux données de Project Server dans les vues et les tables provisoires, publiées et archivées de la base de données Project. Vous pouvez accéder à un service PSI via un fichier de proxy ou un assembly de proxy pour les services WCF ou les services web ASMX.
  
> [!NOTE]
> Le modèle objet client représente l’interface privilégiée pour les développeurs tiers de Project Server ; il peut être utilisé pour les applications qui accèdent à une installation Project Server locale et à Project Online. Nous vous recommandons d’utiliser le modèle objet client pour développer de nouvelles applications, si celui-ci inclut les fonctionnalités dont votre application a besoin. 
  
Certaines applications métier et d’autres applications tierces qui ont été développées pour Project Server 2010 requièrent des services PSI qui ne sont pas encore représentés dans le modèle objet client. Si elles ciblent uniquement une installation locale de Project Server, les applications peuvent continuer à utiliser l’interface WCF ou l’interface ASMX de l’interface PSI.
  
Les applications clientes appellent l’interface PSI via des proxys de service. Les clients qui utilisent l’interface WCF accèdent à tous les services PSI via `https://ServerName/ProjectServerName/_vti_bin/psi/ProjectServer.svc`. Les clients qui utilisent une interface de service web ASMX utilisent l’URL de Project Web App pour le service spécifique. Par exemple, le service **Resource** est à `https://ServerName/ProjectServerName/_vti_bin/psi/resource.asmx?wsdl`. Si les applications n’ont pas un accès intranet à Project Server, elles peuvent utiliser un serveur Project Web App dans un réseau de périmètre (non illustré dans la figure 3).
  
La figure 4 montre le volet **Connexions** dans **Gestionnaire des services Internet (IIS)** pour une installation à serveur unique de SharePoint Server 2013, Project Server 2013 et un site Gestion du flux de travail local pour Workflow Manager Client 1.0. La collection de sites SharePoint (A) inclut les services PSI frontaux dans le sous-répertoire virtuel `_vti_bin\PSI`. L’application Services web SharePoint (B) inclut l’application de service Project, avec les services PSI principaux dans le sous-répertoire virtuel `508c23fb7dfd4c83a8919fae24bc68c5/PSI`. Le GUID est le nom de l’instance de l’application de service Project de cette installation Project Server. 
  
**Figure 4. Gestionnaire des services Internet (IIS) affichant les services PSI frontaux (A) et les services PSI principaux (B)**

![PSI frontal et PSI principal](media/pj15_Architecture_PSI_IIS.gif "PSI frontal et PSI principal")
  
Les applications clientes ne peuvent pas accéder directement aux services WCF pour l’interface PSI dans l’application de service Project principale. Si elles ne requièrent pas d’accès à Project Online, les applications clientes et les composants des applications métier utilisent des proxys pour l’interface PSI. Une URL principale pour l’interface WCF du service **Resource** dans la figure 4, par exemple, pourrait être `https://ServerName:32843/508c23fb7dfd4c83a8919fae24bc68c5/psi/resource.svc`. Le port 32843 est le port HTTP par défaut pour l’application Services web SharePoint (32844 est le port pour les communications HTTPS). Toutefois, le fichier web.config pour Project Web App bloque l’accès direct aux services PSI principaux.
  
> [!NOTE]
> Le téléchargement du kit de développement logiciel (SDK) Project 2013 inclut les fichiers proxy PSI pour les services WCF et ASMX, et des instructions sur la compilation de ces derniers en assemblys de proxy. > Pour créer des fichiers de proxy PSI mis à jour qui utilisent l’interface WCF, vous devez faire appel à l’utilitaire svcutil.exe ou à Visual Studio directement sur l’ordinateur Project Server. 
  
Généralement, les membres des services PSI produisent ou consomment des objets de type **DataSet** pour échanger des informations avec les objets métier. Il existe également plusieurs modèles différents pour le développement PSI. Par exemple, les services PSI **Resource**, **CustomFields** et **LookupTable** utilisent des objets de filtre XML pour la manipulation **DataSet**, contrairement à d’autres services ; certaines méthodes dans le service **Statusing** utilisent un paramètre _changeXml_, contrairement à d’autres méthodes et services. Le modèle CSOM n’utilise pas de jeux de données. Même si le modèle CSOM a un modèle de programmation différent de l’interface PSI et même si vous pouvez utiliser des assemblys .NET ou JavaScript, le développement avec le modèle CSOM est généralement plus simple et plus cohérent que le développement avec l’interface PSI. 
  
Pour plus d’informations sur l’interface PSI, consultez la rubrique [Vue d’ensemble de la référence PSI](project-psi-reference-overview.md). Pour plus d’informations sur le modèle CSOM, consultez la rubrique [Modèle objet côté Client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="business-objects-in-the-wfe-and-the-project-service-application"></a>Objets métier dans le serveur web frontal et l’application de service Project
<a name="pj15_Architecture_BusinessObjects"> </a>

Le modèle objet interne de Project Server inclut des objets métier, qui représentent des entités logiques telles que des projets et des ressources. Les applications clientes accèdent aux objets métier uniquement par le biais de CSOM ou PSI. Les objets métier quant à eux accèdent aux ébauches de tables et d’affichages, et aux tables et affichages publiés et archivés dans la base de données Project.
  
Les objets métier ne sont pas exposés aux développeurs tiers. PSI gère le mappage de l’API aux objets métier, et CSOM mappe son API à PSI. Les entités logiques d’objets métier peuvent être classées en trois catégories :
  
- Les **entités de base** sont des objets tels que des projets, tâches, attributions, ressources et calendriers. Elles incluent la logique métier de base, comme les autorisations et les règles d’attribution de noms. 
    
- Les **entités métier** sont des objets tels que des feuilles de temps, portefeuilles de projets et modèles. Elles incluent une logique métier supplémentaire et sont généralement basées sur une combinaison d’entités de base. 
    
- Les **entités de support** sont des objets tels que la sécurité et la validation. 
    
Dans Project Server 2010, tous les objets métier sont implémentés dans l’application de service Project. Dans Project Server 2013, le serveur web frontal héberge de nombreux objets métier qui traitent les méthodes synchrones et ne requièrent pas le service de calcul Project. Les méthodes PSI synchrones comme **DeleteProject** et **ReadAssignments** n’utilisent pas le service de mise en file d’attente de Project Server. Les méthodes asynchrones dans l’interface PSI portent des noms qui commencent par `Queue`, comme **QueueCreateProject** et **QueueUpdateTimesheet**. Une méthode asynchrone envoie un message au service de mise en file d’attente de Project Server, qui planifie le traitement de la méthode lorsque le contrôle est renvoyé à l’utilisateur.
  
Le redirecteur PSI détermine les requêtes qui sont envoyées à l’application de service Project et qui peuvent être traitées par les objets métier dans le composant web frontal. Les objets métier du composant web frontal ignorent l’application de service Project et ont un accès direct à la base de données Project, tout comme les autres processus SharePoint du composant web frontal accèdent directement aux bases de données de configuration et de contenu. L’exécution de nombreux objets métier du composant web frontal améliore l’efficacité de Project Server, réduit la charge sur le niveau de l’application et permet à Project Server une meilleure mise à l’échelle pour les charges de travail accrues.
  
> [!NOTE]
> Dans Project Server 2013, les gestionnaires d’événements locaux doivent être déployés dans le WFE et sur l’ordinateur Project Server principal. 
  
### <a name="project-server-database"></a>Base de données Project Server
<a name="pj15_Architecture_DAL"> </a>

Dans Project Server 2013, les quatre bases de données Project Server des versions précédentes sont combinées dans une base de données Project dans SQL Server. Le nom de base de données Project par défaut est ProjectService. Les vues et tables de création de rapports conservent leurs noms précédents avec le préfixe `dbo`, comme par exemple, dbo.MSP_EpmProject et dbo.MSP_EpmProject_UserView. Les tables et vues qui figuraient auparavant dans la base de données provisoire ont le préfixe `draft`. Les tables et vues de la base de données publiée ont le préfixe `pub`. Les tables et vues de la base de données archivée ont le préfixe `ver`. 
  
> [!IMPORTANT]
> L’accès direct n’est pas pris en charge pour les tables et les vues provisoires (préfixe `draft`), publiées (préfixe `pub`) et archivées (préfixe `ver`). Les rapports doivent utiliser uniquement les vues et tables de création de rapports, qui ont le préfixe `dbo`. 
  
Les données Project Server sont partitionnées dans la base de données Project de la façon suivante :
  
- Les vues et les tables provisoires contiennent des données provenant de projets non publiés créés par Project Professionnel et d’autres applications. Project Web App n’affiche pas les données de projet provenant de vues et tables provisoires.
    
- Les vues et tables publiées contiennent tous les projets publiés et les ressources d’entreprise, des données globales pour les types de projet d’entreprise et d’autres modèles de projet. Les projets publiés sont visibles dans Project Web App. Les données publiées incluent également des tables qui sont spécifiques à Project Web App (feuilles de temps, modèles, vues, etc.) et des tables de données globales (champs personnalisés, tables de choix, autorisations Project Server et métadonnées).
    
- Les données archivées enregistrent les versions de sauvegarde des projets, ressources, champs personnalisés et autres données.
    
- Les données de création de rapports peuvent être utilisées pour l’accès en lecture seule dans des applications tierces et pour les rapports. Les cubes OLAP Project Server utilisent les vues de création de rapports ayant le suffixe `_OlapView`. Les cubes OLAP sont disponibles dans une installation de Project Server locale, mais ne sont pas disponibles dans Project Online. 
    
    Les données de génération de rapports sont complètes et mises à jour presque en temps réel. Les tables et affichages de génération de rapports sont optimisés pour la génération de rapports en lecture seule ; par exemple, les tables de génération de rapports sont dénormalisées pour fournir des données redondantes et réduire le nombre de tables relationnelles.
    
Les entités logiques telles que les ressources et les projets peuvent être situées dans plusieurs tables, et toutes les tables d’une entité spécifique ont la même clé principale. Cette dernière correspond au GUID d’une colonne unique qui identifie de manière unique une instance spécifique d’une entité donnée.
  
Les données Project Server pour chaque instance de Project Web App sont stockées dans une base de données Project distincte sous un autre nom. Les applications clientes qui ont un accès direct à Project Server peuvent lire directement les tables et vues de création de rapports. Pour un accès à distance, les applications clientes peuvent utiliser l’interface OData et l’interface REST pour obtenir des données pour les rapports. Les clients doivent utiliser uniquement le modèle CSOM ou l’interface PSI pour accéder aux vues et tables provisoires, publiées et archivées. Le service de données de création de rapports (RDS, qui n’apparaît pas dans la figure 3) met à jour les données de création de rapports provenant des données publiées pratiquement en temps réel. La base de données Project peut se trouver sur un serveur distinct.
  
Les schémas sont documentés uniquement pour les tables et vues de création de rapports. Pour une installation de Project Server locale, vous pouvez ajouter des tables et des vues de création de rapports pour des entités non définies dans le schéma de base de données Project. Vous pouvez aussi créer des bases de données distinctes pour des applications locales personnalisées. La modification n’est pas prise en charge pour les tables et les vues provisoires, publiées et archivées. Si votre application ou rapport personnalisé nécessite des objets SQL personnalisés (par exemple, des tables et des vues), nous vous recommandons de créer celles-ci dans une base de données personnalisée. Étant donné que la base de données Project n’est pas directement accessible dans Project Online, les tables et vues de création de rapports ne peuvent pas être modifiées. Toutefois, si vous avez un compte SQL Azure, vous pouvez créer des bases de données distinctes pour une utilisation personnalisée avec Project Online.
  
### <a name="event-receivers"></a>Récepteurs d’événements
<a name="pj15_Architecture_EventHandlers"> </a>

Les gestionnaires d’événements locaux et les récepteurs d’événements distants pour Project Server permettent l’extensibilité tierce en réponse à des événements Project Server tels que la création ou la publication d’un projet. Dans Project Server 2010, tous les gestionnaires d’événements sont locaux et sont écrits en code de confiance totale, déployés directement sur l’ordinateur exécutant Project Server et sur les serveurs web frontaux, et s’exécutent à l’intérieur du système de gestion des événements de Project Server. Étant donné que Project Online ne peut pas utiliser de gestionnaires d’événements de confiance totale, Project Server 2013 implémente des récepteurs d’événements à distance qui sont semblables aux récepteurs d’événements à distance dans SharePoint Server 2013. Une installation de Project Server 2013 locale peut utiliser des gestionnaires d’événements de confiance totale en local et des récepteurs d’événements à distance classiques.
  
Un récepteur d’événements à distance Project Server peut être implémenté dans un service web personnalisé avec un point de terminaison SOAP qui s’exécute dans Microsoft Azure ou d’autres environnements prenant en charge les services web SOAP. Un package d’application Project Server peut inclure des récepteurs d’événements à distance qui sont installés avec l’application.
  
Les récepteurs d’événements à distance peuvent rappeler dans Project Server à l’aide de points de terminaison de modèle CSOM (non illustré dans la figure 3). L’appel à un récepteur d’événements à distance inclut des informations du système d’événements Project Server et de l’instance Project Web App (ou du client Project Web App dans Project Online) qui émet l’appel. Les récepteurs d’événements à distance vous permettent de créer et d’héberger un service web unique qui peut être utilisé par plusieurs installations de Project Server. En revanche, les gestionnaires d’événements de confiance totale locaux doivent être déployés sur chaque installation de Project Server.
  
### <a name="publishing-and-server-side-scheduling"></a>Publication et planification côté serveur
<a name="pj15_Architecture_PublishingScheduling"> </a>

Project Server 2013 prend en charge les mises à jour de planification de projet manuelle et automatisée. Le processus par défaut est une mise à jour de la planification manuelle. Autrement dit, le responsable de projet extrait et ouvre un projet dans Project Professionnel ou Project Web App, applique les modifications puis enregistre et publie le projet pour que les modifications soient disponibles pour tout le monde. Project Professionnel dispose d’un moteur de planification qui calcule les modifications puis les enregistre dans Project Server. Dans Project Server 2010, le moteur de planification côté serveur est une implémentation différente du moteur de planification dans Project Professionnel.
  
Dans Project Server 2013, le Service de calcul de Project implémente le même moteur de planification que celui de Project Professionnel 2013. Le Service de calcul de Project est exécuté dans un service Windows nommé **Service de calcul Microsoft Project Server**. La modification d’une planification de projet dans Project Web App ou à l’aide d’applications tierces qui utilisent le modèle CSOM entraîne exactement les mêmes modifications de planification que celles faites par Project Professionnel.
  
> [!NOTE]
> Les applications tierces qui utilisent l’interface PSI peuvent présenter des différences de planification par rapport à une planification calculée par Project Web App. Pour la compatibilité descendante, les méthodes PSI publiques qui effectuent une planification côté serveur utilisent encore le moteur de planification qui a été introduit dans Project Server 2010. Une exception est **QueueUpdateProject2**, qui est une nouvelle méthode PSI dans Project Server 2013. Par exemple, l’ancien moteur de planification ne planifie pas les sous-projets ou les liens vers d’autres projets et ne calcule pas les champs de valeur acquise. Pour éviter les différences de planification potentielles entre les applications tierces et Project Professionnel ou Project Web App, vous devez développer des applications avec le modèle CSOM autant que possible. 
  
Pour autoriser la mise à jour de la version publiée d’un projet alors qu’un responsable de projet utilise une ébauche de version, Project Server procède comme suit :
  
1. Project Server applique les mises à jour et replanifie la version publiée.
    
2. Project Server enregistre la mise à jour à appliquer à l’ébauche de version lorsque l’un des événements suivants se produit :
    
   - Project Professionnel ouvre le projet.
    
   - Project Professional tente de publier le projet.
    
3. En cas de conflit, le responsable de projet est informé et doit résoudre le conflit avant de pouvoir publier la version provisoire.
    
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de Project 2013 pour les développeurs](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)
- [Programmabilité de Project Server](project-server-programmability.md)  
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)  
- [Fonctionnalités de l’interface PSI](what-the-psi-does-and-does-not-do.md)  
- [Prise en main du développement de flux de travail Project Server](getting-started-developing-project-server-workflows.md)   
- [Vue d’ensemble de la référence Project PSI](project-psi-reference-overview.md)   
- [Open Data Protocol](https://www.odata.org/)
    

