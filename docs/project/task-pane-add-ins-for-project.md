---
title: Compléments du volet Office pour Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 et Project Professionnel 2013 prennent tous les deux en charge les compléments Office du volet Office. Vous pouvez utiliser des compléments du volet Office pour intégrer un projet, une tâche, une ressource et afficher des données dans un projet avec d’autres applications clientes Office 2013, des applications SharePoint, des composants WebPart, d’autres pages web et des données externes.
ms.openlocfilehash: 12e06f364eb1ae6268233c5011fbe451799596be
ms.sourcegitcommit: b9eed77e21325860cef74e4fb8b86adcc247bc09
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2022
ms.locfileid: "66608420"
---
# <a name="task-pane-add-ins-for-project"></a>Compléments du volet Office pour Project

Project Standard 2013 et Project Professionnel 2013 prennent tous les deux en charge les compléments Office du volet Office. Vous pouvez utiliser des compléments du volet Office pour intégrer un projet, une tâche, une ressource et afficher des données dans un projet avec d’autres applications clientes Office 2013, des applications SharePoint, des composants WebPart, d’autres pages web et des données externes.
  
Les compléments Office sont un modèle d’extensibilité pris en charge dans plusieurs applications clientes Office 2013. La plateforme complète de complément inclut des types de complément contextuels, de contenu et de volet Office. Outlook 2013 prend en charge les compléments de messagerie, qui peuvent afficher une page web dans un e-mail ou un élément de rendez-vous de calendrier lié au contenu de l’élément. Word 2013 et Excel 2013 prennent en charge les compléments de contenu, qui peuvent afficher une page web en tant que contenu incorporé dans un document. Word 2013, Excel 2013 et Project Professionnel 2013 prennent en charge les compléments du volet Office, qui peuvent afficher une page web dans un volet Office où le contenu est lié à des informations contextuelles dans le projet.
  
Par exemple, un complément Project peut résumer les données du projet actif et afficher des données supplémentaires sur une tâche ou une ressource sélectionnée. Les données associées dans le complément peuvent provenir d’une source externe telle qu’une liste SharePoint, des tables de rapports dans la base de données Project Server, un service web ou une autre application d’entreprise. Un complément du volet Office peut être développé avec HTML 5, JavaScript, JQuery et d’autres bibliothèques JavaScript. Un complément du volet Office ne prend pas directement en charge les composants ActiveX, Silverlight ou Flash. Bien qu’un complément Office puisse utiliser un élément **IFrame** pour accéder à une application web côté serveur qui utilise ASP.NET et la bibliothèque .NET Framework 4.5, ce type de solution n’est pas recommandé ou pris en charge. Le complément peut être développé pour enregistrer des données localement ou écrire des données dans un emplacement externe.
  
> [!NOTE]
> Les compléments project du volet Office peuvent accéder aux données à partir de Project Online à l’aide de l’authentification OAuth. Avec Project Professionnel 2013, vous pouvez développer des compléments du volet Office qui accèdent aux installations locales de Project Server 2013 et à SharePoint 2013 localement ou en ligne. Par exemple, consultez [Connecting a Project Task Pane add-in to PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) in the Project Programmibility blog. > Project Standard 2013 ne prend pas en charge l’intégration directe avec les données Project Server ou les listes de tâches SharePoint synchronisées avec Project Server.
  
Pour plus d’informations sur les compléments pour Office 2013, consultez [Compléments Office et SharePoint](/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
  
## <a name="developing-task-pane-add-ins"></a>Développement de compléments du volet Office

La documentation des développeurs pour les compléments Office et SharePoint comprend des articles et des références complets. Pour une introduction au développement de compléments pour Project Professionnel 2013 et d’autres applications clientes Office 2013, ainsi que pour la référence JavaScript et la référence du manifeste XML, consultez [Compléments Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
Le téléchargement du Kit de développement logiciel (SDK) Project 2013 inclut l’exemple de complément **Project OM Test** qui montre comment obtenir le GUID d’une tâche, d’une ressource et d’une vue, comment obtenir les propriétés du projet actif et comment définir un gestionnaire d’événements modifié pour une tâche, une ressource ou une vue. Lorsque vous extrayez et installez le Kit de développement logiciel (SDK) et les exemples dans le fichier Project2013SDK.msi, consultez le `\Samples\Apps\Copy_to_AppSource_FileShare` sous-répertoire et le `\Samples\Apps\Copy_to_AppManifests_FileShare` sous-répertoire. L’exemple JSOMCall.html utilise des fonctions JavaScript dans le fichier office.js et le fichier project-15.js, qui sont inclus dans le téléchargement. Vous pouvez utiliser les fichiers de débogage correspondants (office.debug.js et project-15.debug.js) pour examiner les fonctions.
  
**L’exemple de complément HelloProject_OData** pour Project Professionnel 2013 a été développé avec Visual Studio 2012. Le complément utilise une requête REST du service **ProjectData** pour obtenir des données de rapport pour le coût du projet et d’autres informations, puis compare le projet actuel avec les valeurs moyennes de tous les projets dans Project Web App.
  
## <a name="see-also"></a>Voir aussi

<a name="bk_addresources"> </a>

- [Compléments du volet Office pour Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)

- [Connexion d’un complément du volet Tâches de projet à PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)

- [Téléchargement du kit de développement logiciel (SDK) de Project 2013](https://www.microsoft.com/download/details.aspx?id=30435%20)

- [Compléments Office et SharePoint](/sharepoint/dev/sp-add-ins/sharepoint-add-ins)

- [Compléments Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
