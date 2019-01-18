---
title: Dossiers
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecf342c54d1aa2020fbfad4175a220b2aefecbe3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707044"
---
# <a name="folders"></a>Dossiers

Cette section fournit des exemples de tâches qui mettent en œuvre des dossiers. Les objets [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) représentent la hiérarchie des dossiers où les éléments de Microsoft Outlook sont stockés. Calendrier, Courrier et Éléments supprimés sont des exemples de dossiers. Dans l'assembly PIA (Primary Interop Assembly) d'Outlook, les membres de l'objet **Folder** sont exposés en tant que membres de l'objet [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) .

## <a name="in-this-section"></a>Dans cette section

|Rubrique|Description|
|:----|:----------|
|[Ajouter un dossier à la liste des dossiers](how-to-add-a-folder-to-the-folder-list.md) |Utilise la méthode [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) pour ajouter un dossier à la liste des dossiers Outlook.|
|[Énumérer les dossiers](how-to-enumerate-folders.md)  |Énumère les dossiers par itération dans une collection de dossiers.|
|[Obtenir un dossier par défaut et énumérer ses sous-dossiers](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |Obtient un dossier par défaut dans la banque d’informations de l’utilisateur par défaut et énumère ses sous-dossiers.|
|[Obtenir un dossier à partir de son chemin d’accès](how-to-get-a-folder-based-on-its-folder-path.md)  |Prend un chemin d’accès à un dossier et obtient le dossier associé.|
|[Sélectionner un dossier et afficher les informations du dossier](how-to-select-a-folder-and-display-folder-information.md)  |Affiche par programme les informations sur un dossier qu’un utilisateur sélectionne dans une liste des dossiers spécifiée.|
|[Obtenir la classe de message par défaut d’un dossier](how-to-get-the-default-message-class-of-a-folder.md)  |Utilise la propriété [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) pour obtenir la classe de message par défaut d’un dossier.|
|[Accéder aux données spécifiques à la solution stockées comme message masqué dans un dossier](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |Utilise l’objet [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) pour récupérer des données qui sont stockées sous forme de message masqué d’une classe de message spécifique dans un dossier.|
|[S’assurer que les propriétés des éléments personnalisés sont prises en charge dans les requêtes au niveau du dossier](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |Montre comment vous assurer que lorsque vous ajoutez une propriété personnalisée à un type d'élément, vous ajoutez également la propriété au dossier, ce qui vous permet d'effectuer des requêtes sur cette propriété personnalisée au niveau du dossier.|

## <a name="see-also"></a>Voir aussi

- [Calendar](calendar.md)
- [Contacts](contacts.md)
- [Courrier](mail.md)
- [Procédure (Référence PIA Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

