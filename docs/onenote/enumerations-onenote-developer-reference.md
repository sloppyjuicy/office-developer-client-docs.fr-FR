---
title: Énumérations (référence du développeur OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: Cette rubrique décrit les énumérations dans le modèle objet OneNote 2013.
ms.openlocfilehash: 3338e444e5b0bfd0239e363c3161aeb1914b2d53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410335"
---
# <a name="enumerations-onenote-developer-reference"></a>Énumérations (référence du développeur OneNote)

Cette rubrique décrit les énumérations dans le modèle objet OneNote 2013.
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

Lorsqu'elle est transmise à la méthode **OpenHierarchy** , spécifie le type d'objet à créer, le cas échéant, si le chemin d'accès passé à la méthode n'existe pas encore. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |Ne crée pas d'objet.  <br/> |
|**cftNotebook** <br/> |0,1  <br/> |Crée un bloc-notes en utilisant le nom et l'emplacement spécifiés.  <br/> |
|**cftFolder** <br/> |n°2  <br/> |Crée un groupe de sections à l'aide du nom et de l'emplacement spécifiés.  <br/> |
|**cftSection** <br/> |3  <br/> |Crée une section en utilisant le nom et l'emplacement spécifiés.  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indique l'emplacement d'ancrage d'une fenêtre OneNote 2013 à l'aide de l'interface de la [fenêtre](window-interfaces-onenote.md) . Lorsqu'elle a la valeur de la propriété **DockedLocation** , spécifie l'emplacement auquel ancrer une fenêtre OneNote. Cette énumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |La fenêtre OneNote est ancrée à l'emplacement par défaut sur le bureau.  <br/> |
|**dlLeft** <br/> |0,1  <br/> |La fenêtre OneNote est ancrée sur le côté gauche du bureau.  <br/> |
|**dlRight** <br/> |n°2  <br/> |La fenêtre OneNote est ancrée sur le côté droit du bureau.  <br/> |
|**dlTop** <br/> |3  <br/> |La fenêtre OneNote est ancrée en haut du bureau.  <br/> |
|**dlBottom** <br/> |4  <br/> |La fenêtre OneNote est ancrée au bas du bureau.  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Lorsqu'elle est transmise à la méthode **SetFilingLocation** , spécifie le type de contenu pour lequel l'emplacement de classement est défini lorsque le type de contenu est envoyé à OneNote. Cette énumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |Définit l'emplacement de dépôt des messages électroniques Outlook.  <br/> |
|**flContacts** <br/> |0,1  <br/> |Définit l'emplacement où les contacts Outlook seront classés.  <br/> |
|**flTasks** <br/> |n°2  <br/> |Définit l'emplacement où les tâches Outlook seront classées.  <br/> |
|**flMeetings** <br/> |3  <br/> |Définit l'emplacement où les réunions Outlook seront enregistrées.  <br/> |
|**flWebContent** <br/> |4  <br/> |Définit l'emplacement de stockage d'Internet Explorer.  <br/> |
|**flPrintOuts** <br/> |disque  <br/> |Définit l'emplacement de dépôt des documents imprimés à partir de l'imprimante OneNote.  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Lorsqu'elle est transmise à la méthode **SetFilingLocation** , indique où le contenu envoyé à OneNote est enregistré. Cette énumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |Définit le classement du contenu sur une nouvelle page dans une section spécifiée.  <br/> |
|**fltCurrentSectionNewPage** <br/> |0,1  <br/> |Définit le classement du contenu sur une nouvelle page dans la section active.  <br/> |
|**fltCurrentPage** <br/> |n°2  <br/> |Définit le classement du contenu sur la page actuelle.  <br/> |
|**fltNamedPage** <br/> |4  <br/> |Définit le classement du contenu sur une page spécifiée.  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

Lorsqu'elle est assignée à la propriété **TreeDepth** de l'interface [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md) , indique la profondeur de l'arborescence OneNote à afficher lorsque la boîte de dialogue de classement rapide est affichée. Lorsqu'elle est passée à la méthode **AddButton** de l'objet **IQuickFilingDialog** , fait référence à certains éléments de la hiérarchie OneNote. Cette énumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |Fait référence à aucun élément.  <br/> |
|**heNotebooks** <br/> |0,1  <br/> |Fait référence aux éléments de bloc-notes.  <br/> |
|**heSectionGroups** <br/> |n°2  <br/> |Fait référence aux éléments Group de section.  <br/> |
|**heSections** <br/> |4  <br/> |Fait référence aux éléments de section.  <br/> |
|**hePages** <br/> |8bits  <br/> |Fait référence aux éléments de la page.  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Lorsqu'elle est transmise à la méthode **GetHierarchy** , spécifie le niveau le plus bas à obtenir dans la hiérarchie des nœuds du bloc-notes. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |Obtient uniquement le nœud de début spécifié et aucun descendant.  <br/> |
|**hsChildren** <br/> |0,1  <br/> |Obtient les nœuds enfants immédiats du nœud de début et aucun descendant dans les groupes de sous-section supérieur ou inférieur.  <br/> |
|**hsNotebooks** <br/> |n°2  <br/> |Obtient tous les blocs-notes sous le nœud de démarrage ou racine.  <br/> |
|**hsSections** <br/> |3  <br/> |Obtient toutes les sections sous le nœud de début, y compris les sections dans les groupes de sections et les groupes de sous-section.  <br/> |
|**hsPages** <br/> |4  <br/> |Obtient toutes les pages situées sous le nœud de début, y compris toutes les pages dans les groupes de sections et les groupes de sous-section.  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Lorsqu'elle est passée à la méthode **CreateNewPage** , cette énumération spécifie le style de la nouvelle page. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |Crée une page avec le style de page par défaut.  <br/> |
|**npsBlankPageWithTitle** <br/> |0,1  <br/> |Crée une page vierge avec un titre.  <br/> |
|**npsBlankPageNoTitle** <br/> |n°2  <br/> |Crée une page vierge sans titre.  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Lorsqu'elle est transmise à la méthode **NotebookFilterOut** de l'objet **qfd** , spécifie les blocs-notes à afficher lors de l'affichage de la zone de qfd. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |0,1  <br/> |Autoriser uniquement les blocs-notes locaux.  <br/> |
|**nfoNetwork** <br/> |n°2  <br/> |Autorise les blocs-notes UNC ou SharePoint.  <br/> |
|**nfoWeb** <br/> |4  <br/> |Autorise les blocs-notes OneDrive.  <br/> |
|**nfoNoWacUrl** <br/> |8bits  <br/> |Tout bloc-notes sur des emplacements qui n'ont pas de client Web.  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (mis à jour pour OneNote 2013)
<a name="odc_PageInfo"> </a>

Lorsqu'elle est transmise à la méthode **GetPageContent** , spécifie le type d'informations à renvoyer avec le contenu de la page. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |Renvoie uniquement le contenu de la page de base, sans balisage de sélection, les types de fichiers pour les objets de données binaires et les objets de données binaires. Il s'agit de la valeur standard à transmettre.  <br/> |
|**piBinaryData** <br/> |0,1  <br/> |Renvoie le contenu de la page sans balisage de sélection, mais avec toutes les données binaires.  <br/> |
|**piSelection** <br/> |n°2  <br/> |Renvoie le contenu de la page avec balisage de sélection, mais pas de données binaires.  <br/> |
|**piBinaryDataSelection** <br/> |3  <br/> |Renvoie le contenu de la page avec le balisage de sélection et toutes les données binaires.  <br/> |
|**piFileType** <br/> |4  <br/> |Renvoie le contenu de la page avec les informations de type de fichier pour les objets de données binaires.  <br/> |
|**piBinaryDataFileType** <br/> |disque  <br/> |Renvoie le contenu de la page avec les informations de type de fichier pour les objets de données binaires et les objets de données binaires  <br/> |
|**piSelectionFileType** <br/> |6.x  <br/> |Renvoie le contenu de la page avec la balise de sélection et les informations de type de fichier pour les données binaires.  <br/> |
|**piAll** <br/> |7j/7  <br/> |Renvoie tout le contenu de la page.  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Lorsqu'elle est transmise à la méthode **Publish** , indique le format d'affichage de la page publiée. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |La page publiée est au format. One.  <br/> |
|**pfOneNotePackage** <br/> |0,1  <br/> |La page publiée est au format. onepkg.  <br/> |
|**pfMHTML** <br/> |n°2  <br/> |La page publiée est au format. mht.  <br/> |
|**pfPDF** <br/> |3  <br/> |La page publiée est au format. pdf.  <br/> |
|**pfXPS** <br/> |4  <br/> |La page publiée est au format. Xps.  <br/> |
|**pfWord** <br/> |disque  <br/> |La page publiée est au format. doc ou. docx.  <br/> |
|**pfEMF** <br/> |6.x  <br/> |La page publiée est au format EMF (Enhanced Metafile).  <br/> |
|**pfHTML** <br/> |7j/7  <br/> |La page publiée est au format. html. Ce membre est une nouveauté de OneNote 2013.  <br/> |
|**pfOneNote2007** <br/> |8bits  <br/> |La page publiée se trouve au format 2007. un. Ce membre est une nouveauté de OneNote 2013.  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Lorsqu'elle est passée à la méthode **SetRecentResults** de l'objet **IQuickFilingDialog** , cette énumération spécifie la liste de résultats récents à afficher lorsque la boîte de dialogue classement rapide est affichée. Les listes de résultats récentes sont utilisées pour suivre le jeu d'emplacements OneNote que l'utilisateur sélectionne dans la boîte de dialogue classement rapide. Il existe trois listes de résultats récents dans OneNote 2013 qui effectuent le suivi des opérations de classement, de recherche et de liaison des actions. Cette énumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |Ne définit aucune liste de résultats récents à afficher.  <br/> |
|**rrtFiling** <br/> |0,1  <br/> |Définit la liste de résultats récents «filing» à afficher.  <br/> |
|**rrtSearch** <br/> |n°2  <br/> |Définit la liste des résultats récents de recherche à afficher.  <br/> |
|**rrtLinks** <br/> |3  <br/> |Définit la liste de résultats récents «Links» à afficher.  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Lorsqu'elle est passée à la méthode **GetSpecialLocation** , spécifie le chemin d'accès spécial à obtenir. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |Obtient le chemin d'accès à l'emplacement du dossier de dossiers de sauvegarde.  <br/> |
|**slUnfiledNotesSection** <br/> |0,1  <br/> |Obtient le chemin d'accès à l'emplacement du dossier Notes défichier.  <br/> |
|**slDefaultNotebookFolder** <br/> |n°2  <br/> |Obtient le chemin d'accès à l'emplacement du dossier de bloc-notes par défaut.  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Lorsqu'elle est transmise à la méthode **TreeCollapsedState** de l'objet **qfd** , indique si l'arborescence hiérarchique doit être développée ou réduite. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |Définit l'arborescence de hiérarchie de sorte qu'elle soit développée.  <br/> |
|**tcsCollapsed** <br/> |0,1  <br/> |Définit l'arborescence de hiérarchie de sorte qu'elle soit réduite.  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (mis à jour pour OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Lorsqu'il est passé à l'une des méthodes suivantes, spécifie la version du schéma XML OneNote à utiliser:
  
- **OneNote15. application. GetPageContent**
    
- **OneNote15. application. FindMeta**
    
- **OneNote15. application. FindPages**
    
- **OneNote15. application. GetHierarchy**
    
- **OneNote15. application. GetPageContent**
    
- **OneNote15. application. UpdateHierarchy**
    
- **OneNote15. application. UpdatePageContent**
    
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |Référence le schéma OneNote 2007.  <br/> |
|**xs2010** <br/> |0,1  <br/> |Référence le schéma OneNote 2010.  <br/> |
|**xs2013** <br/> |n°2  <br/> |Référence le schéma OneNote 2013.  <br/> |
|**xsCurrent** <br/> |n°2  <br/> |Référence le schéma de la version actuelle de OneNote.  <br/> <br/>**Remarque**: nous vous déconseillons d'utiliser **xsCurrent** dans la plupart des cas, car cela peut entraîner des problèmes de compatibilité avec les futures versions de OneNote. Au lieu de cela, spécifiez la version du schéma que votre application a été conçue pour gérer, par exemple xs2013.           |
   
## <a name="see-also"></a>Voir aussi

- [Référence du développeur OneNote](onenote-developer-reference.md)

