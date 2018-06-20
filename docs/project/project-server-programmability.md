---
title: Programmabilité de Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- events
- PDS
- PDS compatibility
- Project Server databases
- Project Server events
- Project Server Interface
- Project Server workflow
- Project workflow
- PSI
- PSI limitations
- PSI uses
- SharePoint Services
- WF
- workflow
- Workflow Foundation
- WSS
keywords:
- Project 2013, architecture et programmabilité, PSI, projets, les versions, la programmabilité de Project Server, PSI, limitations, Interface de Project Server, non pris en charge générique de compatibilité, Interface de Project Server, fonctionnalités, Interface de Project Server, PDS, Project Server, project les projets, les Versions, les versions, Project Server, les bases de données, Project 2013, plate-forme, Interface de Project Server, utilisez les événements scénarios, Project Server, Project Server, Project Data Service, compatibilité avec PSI, Project Server Interface
localization_priority: Normal
ms.assetid: a93d2153-5132-4289-af51-69350471e248
description: Découvrez les fonctionnalités principales de la programmabilité de Project Server 2013. Cet article contient des informations sur la conversion des applications qui ont été créées pour les versions antérieures de Project Server.
ms.openlocfilehash: c2c03da1e0b7c010d4cad8801f98c0c0cf0b1883
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787933"
---
# <a name="project-server-programmability"></a>Programmabilité de Project Server

Découvrez les fonctionnalités principales de la programmabilité de Project Server 2013. Cet article contient des informations sur la conversion des applications qui ont été créées pour les versions antérieures de Project Server.

Project Server 2013 est conçu pour prendre en charge la plupart des applications qui ont été développées pour Project Server 2010 et de nouvelles solutions pour plusieurs plateformes, où les applications peuvent accéder à la fois en ligne et les installations de Project Server sur site. Applications et les extensions qui ont été développées pour Project Server 2003 ou version antérieure doivent être modifiées pour utiliser le modèle objet côté client (CSOM) ou l’Interface de Project Server (PSI). Applications qui ont été développées pour Office Project Server 2007 ou Project Server 2010 peuvent nécessiter des modifications et recompilation pour utiliser l’interface PSI ; Pour utiliser le modèle CSOM, les applications qui nécessitent une nouvelle conception.
  
La plateforme de Project Server permet de haut niveau de productivité du programmeur en s’appuyant sur SharePoint Server 2013, .NET Framework 4 et le protocole OData avec le modèle CSOM. Les développeurs peuvent étendre Project Web App avec les applications, les composants d’application et les composants WebPart, définir des flux de travail à l’aide de SharePoint Designer 2013 et appliquer des règles métier à l’aide de récepteurs d’événements distants pour les événements Project Server.
  
## <a name="project-server-and-sharepoint-server"></a>Project Server et SharePoint Server
<a name="pj15_Programmability_MOSS"> </a>

Project Web App est construit sur SharePoint Server 2013 et utilise des pages maîtres et les composants WebPart pour le rendre plus facile de créer des applications personnalisées et des solutions de Project Web App. Project Server 2013 intègre profondément SharePoint Server 2013 en tant que la plate-forme de collaboration de project, reporting, site d’administration, sécurité et gestion des flux de travail.
  
Les sites de projet contiennent des informations et des options de collaboration pour où vous pouvez ajouter des applications par défaut qui incluent un projet SharePoint de synthèse, spécialisé répertorie des tâches avec une chronologie, le suivi des problèmes, risques, membres de l’équipe de projet livrables et calendrier de l’équipe, ainsi que les discussions équipe et bibliothèque de documents. Applications personnalisées pour Project Server 2013 fournissent des extensions et la flexibilité pour la collaboration en équipe. Vous pouvez également ajouter des composants d’application pour personnaliser une application, en utilisant le même mécanisme pour ajouter et modifier des composants WebPart lorsque vous modifiez une page. Vous pouvez trouver les sites de projet n’importe où dans la batterie de serveurs SharePoint où Project Server est installé. Pour utiliser d’autres services principaux de SharePoint Server 2013, telles que des Excel Services et la recherche d’entreprise, un administrateur peut activer et configurer les services. 
  
Lorsque vous installez Project Server 2013, vous configurez l’Application de Service Project dans le site de Services Web SharePoint. L’Application de Service Project comprend les services de Windows Communication Foundation (WCF) local et ASMX web de la PSI. Recherche SharePoint et gestion de documents SharePoint autres des exemples d’applications de service. Pour plus d’informations, voir la documentation du développeur SharePoint Server 2013.
  
L’Application de Service Project est un fournisseur de service logique qui peut gérer plusieurs instances de Project Web App. Mise en service du serveur de projet crée un site Project Web App spécifique au sein d’une application web SharePoint. La page d’accueil de Project Web App contient des liens vers la page Centre de projets, page Centre de ressources et la page Business Intelligence Center pour la création de rapports, ainsi qu’une page qui contient une liste des autres applications standards. La figure 1 illustre la commande **Modifier la Page** dans la liste déroulante **paramètres** sur la page d’accueil de Project Web App, qui vous permet d’ajouter ou de modifier les composants WebPart. 
  
> [!NOTE]
> Certaines pages d’administration dans Project Web App, telles que la page Paramètres PWA — ne sont pas modifiables et ne pas afficher la commande **Modifier la Page** . Project Web App n’autorise pas vous permet de modifier des pages à l’aide de SharePoint Designer 2013. Vous pouvez modifier des pages de site de projet avec SharePoint Designer 2013. 
  
**La figure 1. À l’aide du menu Modifier la Page dans Project Web App**

![Modification de la page d’accueil dans Project Web Access] (media/pj15_Programmability_PWAHome.gif "Modification de la page d’accueil dans Project Web Access")
  
Pour accéder à la page Paramètres du Site dans Project Web App, cliquez sur l’icône **paramètres** dans le coin supérieur droit de la page. La page Paramètres du Site ( `http://ServerName/ProjectServerName/_layouts/15/settings.aspx`) permet de modifier l’apparence et le thème du site, ajout de composants WebPart personnalisés et la modification ou la création de pages pour les sites de projet maître.
  
Personnalisation du code dans les pages ASPX, ou la personnalisation des pages maîtres de Project Web App avec SharePoint Designer 2013, n’est pas pris en charge. Personnalisation du code dans les pages de Project Web App peut entraîner des problèmes avec les service packs et mises à jour de Project Server. 
  
### <a name="customization-of-project-web-app-with-sharepoint-packages"></a>Personnalisation de Project Web App avec des packages SharePoint
<a name="pj15_Programmability_CustomizationOfPWA"> </a>

Étant donné que Project Web App est une application SharePoint et les sites de projet sont des sites SharePoint, vous pouvez ajouter des applications personnalisées, composants WebPart, gestionnaires d’événements, champs personnalisés et d’autres fonctionnalités en utilisant les packages (fichiers .wsp) SharePoint ou les applications SharePoint (fichiers .spapp). Un package SharePoint ou un package d’application peut inclure plusieurs entités de Project Server, où les définitions d’entité sont spécifiées dans un fichier elements.xml dans le package.
  
Pour Project Online, vous pouvez ajouter des boutons au ruban Project Web App, mais vous ne pouvez pas supprimer ou renommer des boutons des produits existants, et vous ne pouvez pas créer de nouveaux onglets du ruban. Pour plus d’informations, voir [créer des actions personnalisées à déployer avec les applications pour SharePoint](http://msdn.microsoft.com/en-us/library/office/apps/jj163954%28v=office.15%29.aspx).
  
> [!CAUTION]
> Lorsque vous installez un package SharePoint ou un package d’application, les types d’entité Project Server doivent apparaître dans l’ordre spécifié par le schéma PSEntityProvision.xsd. Sinon, la validation du schéma du package échoue et l’installation s’interrompt. 
  
Le fichier de schéma PSEntityProvision.xsd est disponible dans le téléchargement du Kit de développement Project 2013, dans le `Documentation\Schemas\AppProvisioning` sous-répertoire. La figure 2 illustre l’affichage de l’Explorateur de schémas XML dans Visual Studio du schéma **PSEntityProvision** , où la séquence **LookupTable** est développée. 
  
**La figure 2. Affichage de l’entité Project Server de mise en service de schéma de Visual Studio**

![Affichage du schéma d’entité Project Server] (media/pj15_Programmability_EntitySchema.gif "Affichage du schéma d’entité Project Server")
  
Packages SharePoint installer des fonctionnalités de Project Server peuvent contenir un ou plusieurs fichiers elements.xml qui suivent le schéma **PSEntityProvision** . Les entités Project Server dans un fichier XML doivent apparaître dans l’ordre suivant : 
  
1. Phases de flux de travail
    
2. Tables de recherche
    
3. Champs personnalisés
    
4. Étapes du flux de travail
    
5. Types de projet d’entreprise
    
6. Gestionnaires d'événements
    
Lorsque vous créez un package SharePoint qui contient des entités Project Server, il est possible de placer les définitions d’entité dans plusieurs fichiers elements.xml. Chaque fichier XML peut réussir la validation de schéma sans que les entités de l’intégralité du package ne soient dans l’ordre correct. Par exemple, une entité de champ personnalisé dans le premier fichier XML peut faire référence à une table de recherche dans le second fichier XML. Pendant l’installation, le champ personnalisé ne peut pas être créé, car la table de recherche n’a pas encore été créée.
  
En cas d’échec de l’installation d’un package, les objets qui ont été créés restent dans Project Web App, mais le package n’installe pas complètement. Réinstallation du package peut fonctionner, mais ce n’est pas une bonne expérience pour les clients. Lorsque les définitions de l’entité de couvrir plusieurs fichiers elements.xml, organiser les entités Project Server dans le package SharePoint entière pour vous assurer qu’installation suit l’ordre correct. Avec le schéma PSEntityProvision.xsd dans le téléchargement du Kit de développement Project 2013, il est possible de développer un outil qui vérifie l’ordre prescrit des entités dans les fichiers XML.
  
## <a name="upgrading-applications-with-the-project-server-apis"></a>Mise à niveau d’application avec les API Project Server
<a name="pj15_Programmability_APIs"> </a>

Lorsque vous mettez à niveau une application qui a été développée pour une version antérieure de Project Server, vous pouvez choisir d’utiliser le modèle CSOM ou la PSI pour une interface de programmation qui inclut des méthodes pour créer, lire, mettre à jour et supprimer des entités de projet (les opérations CRUD). Bien que le modèle CSOM appelle en interne la PSI, elle ne remplace pas entièrement toutes les méthodes PSI. Pour les scénarios et les limitations de la PSI et le modèle CSOM, voir [ce que la PSI fait et ne fait pas](what-the-psi-does-and-does-not-do.md) et [que le modèle et ne fait pas](what-the-csom-does-and-does-not-do.md).
  
> [!NOTE]
> Si le modèle comprend les fonctionnalités que requises, nous vous recommandons de mise à niveau d’applications afin d’utiliser le modèle CSOM. Le modèle CSOM permet aux applications à utiliser pour les locaux et les installations en ligne de Project Server 2013. 
  
Si votre application lit principalement des données à partir de Project Server, vous pouvez utiliser les tables et les affichages de rapports dans la base de données Project Server pour un scénario local. Si vous prévoyez d’utiliser l’application avec Project Online, vous pouvez utiliser le protocole OData pour le service **ProjectData** , qui fournit sur site et un accès aux données de création de rapports en ligne. Pour plus d’informations, voir [ProjectData - référence de service OData Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx)
  
### <a name="using-the-psi"></a>Utilisation de l’interface PSI
<a name="pj15_Programmability_PSI"> </a>

La PSI permet aux applications de confiance totale client, y compris les applications métier, Project Web App et Project Professional 2013, pour accéder aux données Project Server au sein d’une batterie de serveurs SharePoint. La PSI est créé et utilisé avec .NET Framework 4 et fournit des avantages comme un environnement de développement connu avec le garbage collection, gestion des erreurs et la sécurité intégrée.
  
L’interface PSI est accessible via les services WCF ou les services web ASMX. L’interface ASMX est basée sur WCF. Chaque service PSI contient généralement une classe de base avec les méthodes CRUD des éléments dans cette classe. Les éléments sont spécifiés par les classes de **jeu de données** connexes. Par exemple, le service **CustomFields** contient la classe **CustomFields** avec les méthodes telles que [CreateCustomFields2](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.CreateCustomFields2.aspx) . Données pour un ou plusieurs champs personnalisés d’entreprise sont spécifiées dans le **CustomFieldDataSet**.
  
> [!NOTE]
> L’interface de services web ASMX de la PSI est déconseillé dans Project Server 2013. Bien que l’interface ASMX est toujours disponible, nouvelles applications qui utilisent la PSI doivent utiliser l’interface WCF, ou, si possible, les nouvelles applications doivent utiliser le modèle CSOM au lieu de la PSI. Futures versions de Project Server nécessite une mise à niveau des applications existantes basées sur ASMX utiliser l’interface WCF de la PSI ou utiliser le modèle CSOM. 
  
Il existe 22 public, documentée services PSI, qui figurent dans l’interface WCF et l’interface ASMX. L’interface PSI inclut également les huit services privées, non documentées. Project Web App et Project Professional utilisent services PSI publics et privés services PSI. L’interface PSI est généralement pris en compte pour faire correspondre les objets métier. Autrement dit, chaque méthode PSI est associé à un objet métier tels que le **calendrier** ou la **ressource**. L’interface PSI est l’interface principale pour les objets métier. Étant donné que la couche métier fournit des composants de la logique métier réutilisables, différentes applications qui interagissent avec des données Project Server utilisent la même logique métier.
  
Méthodes PSI interagissent de manière asynchrone avec Project Server ont des noms qui commencent par la **file d’attente**. Chaque méthode PSI est implémentée avec une interface séparée qu’utilise les données fortement typées. Par exemple, la méthode **QueueCreateProject** dans le service de **projet** accepte le paramètre de _jeu de données_ de type **ProjectDataSet**. La classe **ProjectDataSet** est dérivée du type de **jeu de données** . Un contrôle de type dans l’exécution de .NET Framework et IntelliSense dans l’aide de Visual Studio pour réduire les erreurs dans le développement avec la PSI. Pour obtenir une introduction à la documentation de référence détaillée pour les espaces de noms PSI, classes, méthodes, propriétés, événements et les assemblys connexes, voir [vue d’ensemble de la référence PSI Project](project-psi-reference-overview.md).
  
Project Server 2013 utilise la gestion des exceptions du .NET Framework. Toutes les erreurs sont enregistrées dans le serveur, en haut de la pile PSI. Certaines erreurs envoyer un rapport simple pour le client, par exemple un objet **SoapException** pour l’interface ASMX ou un objet **exception FaultException** pour l’interface WCF. Exceptions peuvent être enregistrées dans le journal des événements et des erreurs également enregistrent un rapport détaillé sur le serveur dans les journaux de suivi du Service de journalisation unifiée (ULS). 
  
Pour les applications locales de confiance totale, l’interface PSI est également extensible. Vous pouvez ajouter un assembly .NET avec un service qui offre de nouvelles fonctionnalités, utilise la même infrastructure de sécurité Project Server et appelle les autres méthodes PSI ou hérite de classes PSI. Une extension PSI peut également fournir l’accès requis à la base de données et à la logique métier pour les nouvelles fonctionnalités.
  
### <a name="using-the-csom"></a>Utilisation du modèle CSOM
<a name="pj15_Programmability_CSOM"> </a>

Avec le modèle CSOM, vous pouvez développer des applications qui accèdent à Project Online ou une installation de Project Server 2013 sur site. Les applications peuvent être distribuées dans une banque Office publique ou un catalogue d’applications privé. Le modèle est conçu pour être une API facile à utiliser qui consomme directement ou de fournit les données par nom avec des requêtes LINQ, plutôt que par les jeux de données de transmission et construction _changeXml_ paramètres ou des paramètres de _filtre_ XML. Le modèle CSOM implémente la fonctionnalité principale de l’Interface Project Server (PSI) pour les entités principales telles que le **projet**, **tâche**, **EnterpriseResource**et **affectation**. Le modèle comprend plusieurs autres entités comme **CustomField**, **LookupTable**, **WorkflowActivities**, **EventHandler**et **QueueJob**, qui prend en charge d’autres fonctionnalités courantes de Project Server.
  
Il peut être utilisé en copiant les ressources suivantes sur votre ordinateur de développement local :
  
- Pour le développement de .NET Framework 4, copiez le `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll` assembly. 
    
  Pour la documentation des classes CSOM et des membres, consultez l’espace de noms [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . Pour un exemple d’application, voir [mise en route avec CSOM et .NET](getting-started-with-the-project-server-csom-and-net.md).
    
- Pour le développement de Microsoft Silverlight, copiez les `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Silverlight.dll` assembly. 
    
- Pour développer des applications pour Windows Phone 8, copiez les `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Phone.dll` assembly. 
    
- Pour utiliser JavaScript pour le développement d’applications web et des applications pour d’autres périphériques, copiez les `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` fichier et le `PS.debug.js` fichier. Pour un exemple d’application web, voir [mise en route avec le modèle objet JavaScript de Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md).
    
Le modèle CSOM appelle en interne la PSI ; Par conséquent, si une tâche ne peut pas l’interface PSI, ni peut le modèle CSOM. Pour les limitations de CSOM, voir [ce que le modèle et ne fait pas](what-the-csom-does-and-does-not-do.md) et [que la PSI fait et ne fait pas](what-the-psi-does-and-does-not-do.md). Pour plus d’informations sur le développement avec le modèle CSOM, voir [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md) et [modèle d’objet côté Client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="porting-applications-built-for-project-server-2003"></a>Portage des applications conçues pour Project Server 2003 
<a name="pj15_Programmability_Porting2003"> </a>

Dans Project Server 2003, de nombreuses données et fonctionnalités sont disponibles uniquement avec Project Professional 2003 ou par accès direct à la base de données. L’interface PSI, introduite dans Project Server 2007, supprime une grande partie de cette restriction. Contrairement au projet PDS (Project Data Service) dans Project Server 2003, l’interface PSI et le modèle CSOM fournissent des interfaces complètes aux objets d’entreprise dans Project Server.
  
Les applications développées pour le service PDS ne sont pas compatibles avec les versions ultérieures de Project Server. Le modèle CSOM et l’interface PSI prévoient une parité fonctionnelle pour le service PDS, mais ne correspondent pas aux méthodes et paramètres PDS.
  
> [!NOTE]
> Étant donné que les applications de service PDS doivent être entièrement repensées pour Project Server 2013, il est recommandé que vous utilisez le modèle CSOM. 
  
Pour plus d’informations sur la compatibilité PDS et guidelines for portage extensions PDS à PSI, voir [Parité PDS dans les Services Web PSI](http://msdn.microsoft.com/library/61a0b0c7-9b74-46d1-87ed-66ffdd8017f8%28Office.15%29.aspx).
  
### <a name="porting-applications-built-for-project-server-2007-and-project-server-2010"></a>Portage des applications conçues pour Project Server 2007 et Project Server 2010
<a name="pj15_Programmability_Porting2007"> </a>

L’interface PSI dans Project Server 2013 est un sur-ensemble du modèle d’objet PSI dans Office Project Server 2007 et Project Server 2010. De nombreuses applications conçues pour les deux versions précédentes de Project Server continuent à fonctionner dans les installations locales confiance totale, local de Project Server 2013. Toutefois, les types suivants d’applications requièrent des mises à jour ou conception :
  
- Utiliser le modèle CSOM pour les applications qui sont adaptées pour une utilisation avec Project Online.
    
- Utilisez le modèle CSOM pour les applications qui sont adaptées aux appareils mobiles et tablettes.
    
- Utiliser le modèle CSOM pour les applications qui sont disponibles en tant qu’applications dans l’Office Store ou un catalogue d’applications privé.
    
- Pour les applications qui modifient la planification de projet, utiliser le modèle CSOM ou modifier l’application à utiliser la méthode PSI [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) . 
    
- Local ou les applications web qui se connectent aux utilisateurs de différentes instances de Project Web App doivent utiliser les paramètres de programmation pour les points de terminaison WCF de CSOM ou de la PSI. Les méthodes sont désapprouvées. Applications doivent utiliser l’authentification OAuth à la place de l’authentification par formulaires et pour une utilisation avec Project Online. Pour plus d’informations, voir [Authorization and authentication pour les applications dans SharePoint 2013](http://msdn.microsoft.com/en-us/library/fp142384%28office.15%29.aspx#FileName_uniquekeyword1).
    
- Les applications qui s’appuient sur ou modifient des paramètres de sécurité Project Server spécifiques.
    
  > [!NOTE]
  > Une installation locale par défaut Project Server 2013 utilise le mode d’autorisation SharePoint, où les paramètres de sécurité Project Server ne sont pas accessibles par le biais de l’interface PSI. Pour modifier le mode d’autorisation Project, consultez la section *Mode d’autorisation SharePoint* dans [Nouveautés pour les professionnels de l’informatique dans Project Server 2013](http://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx#section13). 
  
- De nombreux flux de travail Project Server personnalisés, vous pouvez utiliser SharePoint Designer 2013 pour créer des flux de travail déclaratifs. Pour les flux de travail personnalisés nécessitant une programmation supplémentaire, vous ne devez *pas* utiliser directement les classes ou membres dans l’espace de noms **Microsoft.Office.Project.Server.Workflow** . Au lieu de cela, utilisez la classe [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) dans le modèle CSOM. 
    
- En règle générale, les applications qui utilisent l’emprunt d’identité doivent être réécrit pour utiliser l’interface WCF de la PSI. Applications qui effectuent des mises à jour d’état simple pour d’autres utilisateurs ne nécessitent pas l’emprunt d’identité. Ils peuvent utiliser la méthode [StatusAssignment.SubmitStatusUpdates](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.StatusAssignment.SubmitStatusUpdates.aspx) dans le modèle CSOM ou la méthode [Statusing.SubmitStatusForResource](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.SubmitStatusForResource.aspx) dans l’interface PSI. 
    
- Composants logiciels intermédiaires qui s’exécutent sur l’ordinateur Project Server peuvent être installés uniquement pour une utilisation locale et doivent utiliser l’interface WCF de la PSI. Par exemple, un composant de logiciels intermédiaires qui utilise le ASMX interface pour échanger des données entre Project Web App sur site et une application de feuilles de temps externes devrait être réécrites pour utiliser l’interface WCF de la PSI. Pour travailler avec Project Online, le composant devrait être modifiée comme une application et utiliser le modèle CSOM.
    
### <a name="migration-and-compatibility-of-custom-solutions"></a>Migration et compatibilité des solutions personnalisées
<a name="pj15_Programmability_CustomSolutions"> </a>

Classes et membres dans les interfaces ASMX et WCF publiques de l’interface PSI sont identiques. Mais, le nombre de colonnes et la taille des tables de données utilisée ou renvoyés par les méthodes PSI peuvent être différentes pour les deux versions précédentes de Project Server et de Project Server 2013. Il existe également des différences dans les tables et les affichages, par rapport à la base de données de création de rapports dans les versions précédentes de création de rapports.
  
> [!IMPORTANT]
> Il est vivement recommandé de tester des solutions sur une installation hors production de Project Server 2013 avant de les déployer sur un serveur de production. 
  
Lorsque vous migrez une solution vers Project Server 2013, ou si une solution ne fonctionne pas comme prévu, vous devez au minimum, procédez comme suit :
  
- Mettre à jour la solution à l’ouvrir dans Visual Studio 2012. Certaines solutions peuvent également utiliser Visual Studio 2010.
    
- Modifier la cible sur .NET Framework 4.
    
- Modifier les références d’assembly à utiliser les assemblys de Project Server 2013, telles que Microsoft.Office.Project.Server.Library.dll et Microsoft.Office.Project.Server.Events.Receivers.dll.
    
- Dressez la liste des références web ASMX ou des références de services WCF et des espaces de noms et supprimez les références Project Server.
    
- Ajoutez l’assembly de proxy ProjectServerServices.dll que vous pouvez créer des fichiers source proxy WCF dans le téléchargement du Kit de développement Project 2013, ou ajouter les fichiers de source de proxy pour les services WCF requis. Pour les services ASMX, ajoutez à nouveau les références de service web ASMX frontal en utilisant les mêmes noms d’espace de noms ; ou ajouter l’assembly de proxy ProjectServerServices.dll que vous pouvez créer à partir des sources dans le téléchargement du Kit de développement Project 2013 WSDL.
    
  > [!NOTE]
  > Dans le téléchargement du Kit de développement Project 2013, les espaces de noms dans la source de proxy fichiers commencent tous par *Svc* . Par exemple, l’espace de noms **ressources** service, dans le fichier de proxy WCF et dans le fichier de proxy ASMX est **SvcResource**. > Si votre application utilise des noms d’espace de noms différent, vous pouvez recompiler l’assembly de proxy pour utiliser vos espaces de noms ou modifier les espaces de noms PSI dans votre application. Par exemple, vous pouvez modifier le script CompileWCFProxyAssembly.cmd et recompiler ProjectServerServices.dll à partir des fichiers source proxy dans le téléchargement SDK. 
  
- Si vous modifiez à partir de l’aide de l’interface ASMX de l’interface PSI à l’interface WCF, vous pouvez initialiser les classes de client par programme ou à l’aide de points de terminaison WCF dans app.config. Utilisez l’initialisation par programme lorsque vous avez passer rapidement à différentes instances de Project Web App, ou lorsque vous développez un composant WebPart qui utilise l’interface PSI.
    
- Il existe plusieurs nouvelles méthodes et jeux de données dans les services PSI dans Project Server 2013 et quelques classes **DataRow** contiennent des nouvelles propriétés. Par exemple, la méthode [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) dans l’interface PSI utilise Project Server moteur de planification pour replanifier un projet mis à jour sans avoir à ouvrir le projet dans Project Professional 2013 et permet également d’ajouter ou de supprimer des entités de projet dans le même appel. 
    
- Compilez et testez la solution.
    
## <a name="project-scheduling-on-the-server"></a>Planification de projets sur le serveur
<a name="pj15_Programmability_Scheduling"> </a>

Project Server 2013 a deux moteurs de planification. Le moteur de planification plus récent est la même que le moteur de planification dans Project Professional 2013. Lorsque vous apportez des modifications de planification et publiez les modifications apportées à l’aide du composant WebPart de planification (page de détails du projet) dans Project Web App ou d’un site de projet, ou à l’aide du modèle CSOM, le calcul de dates, les coûts, durée, travail restant, planifications et autres modifications liées à la planification sont les mêmes que si vous apporté les modifications et publié le projet à l’aide de Project Professional 2013. Toutefois, à l’exception de la méthode [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) , méthodes PSI utilisent le moteur de planification plus ancien qui ont été migré à partir de Project Server 2010. Le fait pour vous assurer que les applications héritées identique dans Project Server 2013 comportent comme précédemment. 
  
> [!NOTE]
> Pour utiliser le moteur de planification mis à jour dans Project Server 2013, les applications peuvent utiliser le modèle CSOM. 
  
Les deux moteurs (ancien et nouveau) de planification possèdent les restrictions suivantes :
  
- **Projet unique planification uniquement** Planification affecte uniquement le projet actif, lorsque des modifications sont apportées par le biais de mises à jour de l’état de tâches avec l’interface PSI ou le modèle CSOM ou Project Web App. Si le projet actif comporte des liens vers d’autres projets, sous-projets ou projets maîtres, les projets liés ne sont pas modifiées. 
    
- **Tâches récapitulatives** Tâches récapitulatives sont généralement en lecture seule dans Project Server. Par exemple, les affectations de tâches récapitulatives ne peut pas être créées et pourcentage d’achèvement ne peut pas être modifié. Toutefois, Project Server prend en charge la modification de la date et la durée des tâches récapitulatives planifiées manuellement. 
    
    Les données réelles dans Project Server ne sont pas ajoutées automatiquement à une affectation de tâche récapitulative, car cela contournerait le processus d’approbation dans Project Server. Dans Project Professionnel, lorsque vous ajoutez des données réelles à une tâche subordonnée, ces données sont également ajoutées pour une affectation sur la tâche récapitulative. La différence de comportement peut être source de confusion pour un utilisateur.
    
    Project Server supprime les données réelles sur une affectation de tâche récapitulative si la durée de la tâche subordonnée diminue ou si la date de fin est modifiée.
    
    > [!CAUTION]
    > Bien que Project Professionnel puisse le faire, nous vous recommandons de ne pas émettre d’affectations sur les tâches récapitulatives. 
  
Voici les problèmes et limitations de la programmation PSI avec l’ancien moteur de planification Project Server :
  
- **Modification de l’état actif d’une tâche** Le moteur de planification Project Server antérieur incohérente Démarrer pour afficher ou fin lorsque vous utilisez la méthode [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) pour modifier l’état actif d’une tâche, s’il existe plusieurs modifications dans l’objet **ProjectDataSet** pour la _ jeu de données_ paramètre. Si la propriété **TASK_IS_ACTIVE** est le seul changement dans le paramètre de _jeu de données_ de **QueueUpdateProject**, vous pouvez mettre à jour le projet.
    
    Pour plus d’informations sur les tâches inactives et l’ancien moteur de planification, voir le blog de l’article [Introduction les tâches inactives dans Project 2010](http://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx) et [Project Server 2010 : planification sur le site web, la PSI et Project Professional](http://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0). Pour obtenir une comparaison de planification dans Project Professionnel 2010 et Project Web App dans Project Server 2010, voir [comparaison de gestion de planification sur le Web](http://www.microsoft.com/project/en/us/project-server-2010-editions.aspx).
    
- **Audit des coûts pas calculée** L’ancien moteur de planification ne calcule pas les champs de la valeur acquise : CRTE, arrière, CBTE, CBTP, IPC, CV, VC %, CAE, SPI, SV, VP %, TCPI, VAC, variation de durée, variation de début, variation de fin, variation de coût et variation de travail. Si un projet a des valeurs de ces champs et le projet est mis à jour à l’aide de la méthode **QueueUpdateProject** , les valeurs de champ ne modifiez pas. Pour éviter ce problème, utilisez la méthode **QueueUpdateProject2** . 
    
Vous pouvez gérer les limitations de la planification PSI des façons suivantes :
  
- Si le modèle CSOM possède les méthodes que requiert l’application, utilisez-le au lieu de l’interface PSI.
    
- Ouvrez des projets dans Project Professionnel et réenregistrez-les sur Project Server.
    
- Dans les rapports, n’incluez pas les champs que l’interface PSI ne met pas à jour.
    
- Ajoutez une note dans les rapports au sujet des données qui peuvent être obsolètes.
    
Il existe des indicateurs dans les tables de création de rapports et les cubes qui vous aident à détecter lorsque certaines données de projet ne sont pas mises à jour. Les données de rapport dans la table MSP_EpmProject et dans MSP_EpmProject_UserView comprennent les champs suivants :  
  
-  _ProjectWbsIsStale_ &ndash; Indique si la structure de répartition du travail (hiérarchie de tâches) est obsolète. 
    
-  _ProjectEarnedValueIsStale_ &ndash; Indique les champs d’audit des coûts sont obsolètes. 
    
-  _ProjectRollupsAreStale_ &ndash; Indique un sous-projet est mis à jour dans la base de données provisoire, mais le projet principal n’est pas mis à jour. Les valeurs reportées du sous-projet sont obsolètes. 
    
-  _ProjectHierarchyNotSynchronized_ &ndash; Le projet principal n’est pas synchronisé avec ses enfants. Cela se produit lorsque les projets enfants sont publiées explicitement, pas dans le cadre de la publication du projet principal. 
    
-  _ProjectCalculationsAreStale_ &ndash; Project professionnel enregistré un projet sans le calcul de la planification (autrement dit, le mode de calcul est défini sur **manuel** sous l’onglet **prévisions** de la boîte de dialogue **Options de projet** ). 
    
-  _ProjectGhostTaskAreStale_ &ndash; Similaire à _ProjectHierarchyNotSynchronized_, mais avertit sur les données des liaisons entre projets. Il est possible que n’existe aucun projet principal, mais les données de projet sur un côté du lien sont plus récentes que celle de l’autre côté.
    
## <a name="about-accessing-the-project-server-database"></a>À propos de l’accès à la base de données Project Server
<a name="pj15_Programmability_Databases"> </a>

Si vous disposez des autorisations dans Microsoft SQL Server pour accéder à la base de données Project Server, vous pouvez lire les tables et les affichages de rapports. Si vous disposez des autorisations nécessaires Project Server, vous pouvez également lire des données à partir des tables de création de rapports à l’aide de requêtes OData. Les développeurs sont fortement déconseillés d’accéder directement à la brouillon, publiée, ou archiver des tables de requêtes SQL Server dans la base de données Project Server. Apporter des modifications directes dans une des tables de la base de données Project Server peut endommager l’intégrité référentielle et interférer avec accès via le Service de mise en attente de Project Server la base de données.
  
> [!IMPORTANT]
> Rien ne vous empêche d’utiliser l’accès direct à la base de données par programme pour mettre à jour les données. Vous devez être conscient que le cache Project Professionnel, les tables publiées et les tables de création de rapports reposent sur un protocole de synchronisation de cache qui peut être perturbé par la modification directe de données. Toutefois, si vous endommagez vos bases de données Project Server ou les caches côté client Project Professionnel suite à un accès direct pour modifier les données, notez que le support technique ne sera pas en mesure de vous aider. 
  
Les applications qui accèdent directement à l’ébauche, publiée ou archiver des tables et affichages dépendent également les schémas de base de données, ce qui peuvent changer dans les service packs ou versions ultérieures de Project Server 2013. Applications qui accèdent directement les bases de données perdent également la sécurité intégrée à Project Server, une logique métier courante, suivi, audits, vérification des erreurs, création de rapports, flux de travail et d’autres fonctionnalités. Vous devrez probablement réécrire ce type d’application après la mise à jour de Project Server 2013. 
  
Pour toutes ces raisons, Project Professionnel et Project Web App ne pas émettre des appels directs au brouillon, publiée, ou archiver des tables ; ne doit être n’importe quelle autre application qui s’intègre avec Project Server.
  
Les schémas pour le brouillon, publiée, et les tables d’archivage ne sont pas documentés. Vous pouvez utiliser les tableaux de création de rapports pour aider à générer des rapports, et le schéma pour les tables et les affichages de rapports est documenté dans le téléchargement du Kit de développement Project 2013. Pour le schéma OData des données de création de rapports, voir [ProjectData - référence de service OData Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
  
## <a name="see-also"></a>Voir aussi

- [Mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md)    
- [Architecture de Project Server 2013](project-server-2013-architecture.md)    
- [Ce que fait la PSI et ne fait pas](what-the-psi-does-and-does-not-do.md)   
- [Ce que fait le modèle CSOM et ne fait pas](what-the-csom-does-and-does-not-do.md)    
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)    
- [Prise en main développement flux de travail Project Server](getting-started-developing-project-server-workflows.md)    
- [Références de programmation de Project 2013](project-2013-programming-references.md)    
- [Présentation des références de projet PSI](project-psi-reference-overview.md)    
- [Créer des actions personnalisées à déployer avec des applications pour SharePoint](http://msdn.microsoft.com/en-us/library/office/apps/jj163954%28v=office.15%29.aspx)    
- [Présentation des tâches inactives dans Project 2010](http://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)    
- [Project Server 2010 : Planification sur le site Web, la PSI et Project Professional](http://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0)
- [Comparaison de gestion de planification sur le Web](http://www.microsoft.com/project/en/us/project-server-2010-editions.aspx)
    

