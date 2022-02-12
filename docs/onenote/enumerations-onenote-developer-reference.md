---
title: Enumerations (référence OneNote développeur)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: Cette rubrique décrit les éumérations dans le modèle objet OneNote 2013.
ms.openlocfilehash: 2a3895980e804cbe5b81614196cce242632cede2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784467"
---
# <a name="enumerations-onenote-developer-reference"></a>Enumerations (référence OneNote développeur)

Cette rubrique décrit les éumérations dans le modèle objet OneNote 2013.
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

Lorsqu’il est transmis à la méthode **OpenHierarchy** , spécifie le type d’objet à créer, le cas contraire, si le chemin d’accès transmis à la méthode n’existe pas encore. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |Ne crée aucun nouvel objet. |
|**cftNotebook** <br/> |1  <br/> |Crée un bloc-notes à l’aide du nom et de l’emplacement spécifiés. |
|**cftFolder** <br/> |2  <br/> |Crée un groupe de sections à l’aide du nom et de l’emplacement spécifiés. |
|**cftSection** <br/> |3  <br/> |Crée une section à l’aide du nom et de l’emplacement spécifiés. |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indique l’emplacement d’accueil d’OneNote 2013 à l’aide de [l’interface Window](window-interfaces-onenote.md). Lorsqu’elle est définie sur **la propriété DockedLocation**, spécifie l’emplacement auquel ancrer une OneNote fenêtre. Cette éumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |La OneNote est fixe à l’emplacement par défaut sur le Bureau. |
|**dlLeft** <br/> |1  <br/> |La OneNote est fixe sur le côté gauche du Bureau. |
|**dlRight** <br/> |2  <br/> |La OneNote est fixe sur le côté droit du Bureau. |
|**dlTop** <br/> |3  <br/> |La OneNote fenêtre est fixe en haut du Bureau. |
|**dlBottom** <br/> |4  <br/> |La OneNote est fixe au bas du Bureau. |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Lorsqu’il est transmis à la **méthode SetFilingLocation**, spécifie le type de contenu pour le lieu de classement lorsque le type de contenu est envoyé à OneNote. Cette éumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |Définit l’Outlook les messages électroniques seront classés. |
|**flContacts** <br/> |1  <br/> |Définit l’Outlook les contacts seront classés. |
|**flTasks** <br/> |2  <br/> |Définit où Outlook tâches seront classées. |
|**flMeetings** <br/> |3  <br/> |Définit l’Outlook les réunions seront classées. |
|**flWebContent** <br/> |4  <br/> |Définit l’endroit où le contenu d’Internet Explorer sera classé. |
|**flPrintOuts** <br/> |5  <br/> |Définit l’endroit où les impressions de l’imprimante OneNote seront classées. |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Lorsqu’il est transmis à **la méthode SetFilingLocation**, spécifie l’endroit où le contenu envoyé OneNote est classé. Cette éumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |Définit le contenu à déposer sur une nouvelle page dans une section spécifiée. |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |Définit le contenu à déposer sur une nouvelle page de la section en cours. |
|**fltCurrentPage** <br/> |2  <br/> |Définit le contenu à déposer sur la page actuelle. |
|**fltNamedPage** <br/> |4  <br/> |Définit le contenu à déposer sur une page spécifiée. |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

Lorsqu’elle est affectée à la propriété **TreeDepth** de l’interface [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md), spécifie la profondeur de l’arborescence OneNote à afficher lorsque la boîte de dialogue de classement rapide est affichée. Lorsqu’elle est transmise à la méthode **AddButton** de l’objet **IQuickFilingDialog**, elle fait référence à certains éléments de la OneNote hiérarchique. Cette éumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |Ne fait référence à aucun élément. |
|**heNotebooks** <br/> |1  <br/> |Fait référence aux éléments notebook. |
|**heSectionGroups** <br/> |2  <br/> |Fait référence aux éléments du groupe de sections. |
|**heSections** <br/> |4  <br/> |Fait référence aux éléments Section. |
|**hePages** <br/> |8   <br/> |Fait référence aux éléments Page. |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Lorsqu’il est transmis à **la méthode GetHierarchy** , spécifie le niveau le plus bas à obtenir dans la hiérarchie de nœuds de bloc-notes. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |Obtient uniquement le nœud de début spécifié et aucun descendant. |
|**hsChildren** <br/> |1  <br/> |Obtient les nœuds enfants immédiats du nœud de début et aucun descendant dans les groupes de sous-sections supérieurs ou inférieurs. |
|**hsNotebooks** <br/> |2  <br/> |Obtient tous les blocs-notes sous le nœud de démarrage ou la racine. |
|**hsSections** <br/> |3  <br/> |Obtient toutes les sections sous le nœud de début, y compris les sections des groupes de sections et des groupes de sous-sections. |
|**hsPages** <br/> |4  <br/> |Obtient toutes les pages sous le nœud de démarrage, y compris toutes les pages des groupes de sections et des groupes de sous-sections. |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Lorsqu’il est transmis à **la méthode CreateNewPage** , spécifie le style de la nouvelle page. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |Crée une page qui a le style de page par défaut. |
|**npsBlankPageWithTitle** <br/> |1  <br/> |Crée une page vierge avec un titre. |
|**npsBlankPageNoTitle** <br/> |2  <br/> |Crée une page vierge sans titre. |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Lorsqu’il est transmis à la méthode **NotebookFilterOut** de l’objet **QFD** , spécifie les blocs-notes à afficher lorsque la zone QFD est affichée. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |Autoriser uniquement les blocs-notes locaux. |
|**nfoNetwork** <br/> |2  <br/> |Autorise les blocs-notes UNC SharePoint portables. |
|**nfoWeb** <br/> |4  <br/> |Permet d OneDrive blocs-notes. |
|**nfoNoWacUrl** <br/> |8   <br/> |Tous les blocs-notes dans les emplacements qui n’ont pas de client web. |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (mise à jour OneNote 2013)
<a name="odc_PageInfo"> </a>

Lorsqu’il est transmis à **la méthode GetPageContent** , spécifie le type d’informations à renvoyer avec le contenu de la page. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |Renvoie uniquement le contenu de page de base, sans marques de sélection, les types de fichiers pour les objets de données binaires et les objets de données binaires. Il s’agit de la valeur standard à transmettre. |
|**piBinaryData** <br/> |1  <br/> |Renvoie le contenu de la page sans marques de sélection, mais avec toutes les données binaires. |
|**piSelection** <br/> |2  <br/> |Renvoie le contenu de la page avec le code de sélection, mais pas de données binaires. |
|**piBinaryDataSelection** <br/> |3  <br/> |Renvoie le contenu de la page avec le code de sélection et toutes les données binaires. |
|**piFileType** <br/> |4  <br/> |Renvoie le contenu de la page avec les informations de type de fichier pour les objets de données binaires. |
|**piBinaryDataFileType** <br/> |5  <br/> |Renvoie le contenu de la page avec les informations de type de fichier pour les objets de données binaires et les objets de données binaires  <br/> |
|**piSelectionFileType** <br/> |6   <br/> |Renvoie le contenu de la page avec le code de sélection et les informations de type de fichier pour les données binaires. |
|**piAll** <br/> |7   <br/> |Renvoie tout le contenu de la page. |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Lorsqu’il est transmis **à la méthode Publish** , spécifie le format dans lequel la page publiée s’affiche. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |La page publiée est au format .one. |
|**pfOneNotePackage** <br/> |1  <br/> |La page publiée est au format .onepkg. |
|**pfMHTML** <br/> |2  <br/> |La page publiée est au format .mht. |
|**pfPDF** <br/> |3  <br/> |La page publiée est au format .pdf format. |
|**pfXPS** <br/> |4  <br/> |La page publiée est au format .xps. |
|**pfWord** <br/> |5  <br/> |La page publiée est au format .doc ou .docx format. |
|**pfEMF** <br/> |6   <br/> |La page publiée est au format métafichier amélioré (.emf). |
|**pfHTML** <br/> |7   <br/> |La page publiée est au format .html format. Ce membre est nouveau dans OneNote 2013. |
|**pfOneNote2007** <br/> |8   <br/> |La page publiée est au format .one 2007. Ce membre est nouveau dans OneNote 2013. |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Lorsqu’il est transmis à la méthode **SetRecentResults** de l’objet **IQuickFilingDialog** , spécifie la liste des résultats récents à afficher lorsque la boîte de dialogue Classement rapide est affichée. Les listes de résultats récents sont utilisées pour suivre l’ensemble des emplacements OneNote que l’utilisateur sélectionne dans la boîte de dialogue Classement rapide. Il existe trois listes de résultats récents dans OneNote 2013 qui font le suivi des actions de classement, de recherche et de liaison. Cette éumération est une nouveauté de OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |Ne définit aucune liste de résultats récents à restituer. |
|**rrtFiling** <br/> |1  <br/> |Définit le rendu de la liste des résultats récents « Classement ». |
|**rrtSearch** <br/> |2  <br/> |Définit la liste des résultats récents « Rechercher » à restituer. |
|**rrtLinks** <br/> |3  <br/> |Définit la liste des résultats récents « Links » à restituer. |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Lorsqu’il est transmis **à la méthode GetSpecialLocation** , spécifie le chemin d’accès d’emplacement spécial à obtenir. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |Obtient le chemin d’accès à l’emplacement du dossier Dossiers de sauvegarde. |
|**slUnfiledNotesSection** <br/> |1  <br/> |Obtient le chemin d’accès à l’emplacement du dossier Notes non filtrées. |
|**slDefaultNotebookFolder** <br/> |2  <br/> |Obtient le chemin d’accès à l’emplacement du dossier du bloc-notes par défaut. |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Lorsqu’il est transmis à la **méthode TreeCollapsedState** de l’objet **QFD** , spécifie si l’arborescence hiérarchique doit être étendue ou réduire. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |Définit l’arborescence hiérarchique à développer. |
|**tcsCollapsed** <br/> |1  <br/> |Définit l’arborescence hiérarchique sur Collapsed. |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (mise à jour OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Lorsqu’il est transmis à l’une des méthodes suivantes, spécifie la version du OneNote XML à utiliser :
  
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.FindMeta**
    
- **OneNote15.Application.FindPages**
    
- **OneNote15.Application.GetHierarchy**
    
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.UpdateHierarchy**
    
- **OneNote15.Application.UpdatePageContent**
    
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |Fait référence au OneNote 2007. |
|**xs2010** <br/> |1  <br/> |Fait référence au OneNote 2010. |
|**xs2013** <br/> |2  <br/> |Fait référence au OneNote 2013. |
|**xsCurrent** <br/> |2  <br/> |Fait référence au schéma de la version OneNote actuelle. <br/>**REMARQUE** : dans la plupart des cas, nous vous déconseillons d’utiliser **xsCurrent**, car cela peut entraîner des problèmes de compatibilité avec les futures versions de OneNote. Spécifiez plutôt la version du schéma que votre application a été conçue pour gérer, comme xs2013.           |
   
## <a name="see-also"></a>Voir aussi

- [Référence du développeur OneNote](onenote-developer-reference.md)

