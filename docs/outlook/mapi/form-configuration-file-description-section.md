---
title: Section Fichier de configuration de formulaire [Description]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
ms.openlocfilehash: 8dda14f4704c9baa4d7905adb5b323bae5373b3e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377903"
---
# <a name="form-configuration-file-description-section"></a>Section Fichier de configuration de formulaire [Description]
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Description]** répertorie toutes les propriétés du formulaire associées aux contrôles dans l’interface utilisateur du formulaire, ainsi que les attributs utilisés pour localiser le formulaire. Les **entrées MessageClass**, **Clsid** et **DisplayName** , qui identifient respectivement le nom de la classe de message du formulaire, son GUID et le nom complet de la classe de message, sont des entrées obligatoires utilisées pour localiser le formulaire dans la bibliothèque de formulaires. Les entrées restantes sont facultatives. Le format de la section **[Description]** est le suivante : 
  
La section **[Description]** répertorie toutes les propriétés du formulaire associées aux contrôles dans l’interface utilisateur du formulaire, ainsi que les attributs utilisés pour localiser le formulaire. Les **entrées MessageClass**, **Clsid** et **DisplayName** , qui identifient respectivement le nom de la classe de message du formulaire, son GUID et le nom complet de la classe de message, sont des entrées obligatoires utilisées pour localiser le formulaire dans la bibliothèque de formulaires. Les entrées restantes sont facultatives. Le format de la section **[Description]** est le suivante : 
  
 **[Description] MessageClass** =   _string_
  
 **Clsid** =   _guid_
  
 **DisplayName** =   _displayedstring_
  
 **SmallIcon** =   _chemin d’accès_
  
 **LargeIcon** =   _chemin d’accès_
  
Les entrées facultatives sont :
  
 **Catégorie** =   _chaîne affichée_
  
 **Sous-catégorie** =   _chaîne affichée_
  
 **Commentaire** =   _chaîne affichée_
  
 **Propriétaire** =   _chaîne affichée_
  
 **Number** =   _chaîne affichée_
  
 **Version** =   _integer_
  
 **Paramètres régionaux** =   _string_
  
 **Hidden** =   _integer_
  
 **DesignerToolName** =   _string_
  
 **DesignerToolGuid** =   _clsid_
  
 **DesignerRuntimeGuid** =   _clsid_
  
 **ComposeInFolder** =   _0|1_
  
 **ComposeCommand** =   _string_
  
Les **entrées** **Catégorie et** Sous-catégorie sont utilisées par les programme d’installation de formulaires pour configurer la catégorisation par défaut des formulaires dans l’interface utilisateur de l’application cliente. Par exemple, une hiérarchie peut être définie où « Help Desk » est la catégorie et « Software » et « Hardware » sont les sous-catégories. Cette catégorisation peut ensuite être utilisée par les applications de visionneuse pour afficher les messages de manière plus organisée. Les **entrées Comment**, **Propriétaire** et **Nombre** sont toutes des chaînes de commentaires qui apparaissent dans l’interface utilisateur de l’application cliente. Ce sont des propriétés spécifiques au formulaire qui peuvent être utilisées à la discrétion du développeur du formulaire. Par exemple, l’entrée Commentaire peut être utilisée pour indiquer l’objectif du formulaire,  l’entrée Propriétaire utilisée pour indiquer la personne ou l’organisation responsable de la maintenance du formulaire et le numéro utilisé pour suivre la version différente du formulaire. Pour **l’entrée** Commentaire, vous pouvez inclure jusqu’à dix lignes de commentaires. La première ligne de commentaires utilise le mot « Comment » comme clé, la deuxième ligne utilise « Comment1 » comme clé, et ainsi de suite par le biais de « Comment9 ». 
  
Les entrées **LargeIcon** et **SmallIcon** sont utilisées pour spécifier le chemin d’accès aux ressources d’icônes utilisées pour afficher les icônes dans l’interface utilisateur de l’application cliente, généralement pour les lignes de tableau qui incluent les colonnes de **propriétés PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Les noms de fichier d’icône peuvent être spécifiés en tant que chemins d’accès par rapport au répertoire où le fichier de configuration du formulaire est installé. **L’entrée** Version est utilisée pour indiquer le numéro de version du formulaire. **Locale est** l’identificateur de langue à trois lettres de la bibliothèque de formulaires de destination. Vous pouvez trouver la liste de ces identificateurs dans la Référence du _programmeur Win32_.
  
**L’entrée** Masquée indique si le formulaire doit être affiché dans l’interface utilisateur d’un fournisseur de bibliothèque de formulaires : 1 indique que le fichier est masqué et 0 indique que le formulaire est visible. Voici un exemple de fichier de configuration de formulaire. 
  
L’entrée **ComposeInFolder** contrôle si le formulaire est conçu pour être placé dans le dossier actuel ou dans la boîte de réception de l’utilisateur lorsque l’utilisateur enregistre le message lors de sa composition : 1 indique que le formulaire doit être placé dans le dossier actuel et 0 indique qu’il doit être placé dans la boîte de réception. 
  
**L’entrée ComposeCommand** est la chaîne à placer dans le menu composition de l’application cliente. Si ce n’est pas spécifié, **l’entrée DisplayName** est utilisée. 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


