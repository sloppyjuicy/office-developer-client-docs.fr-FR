---
title: Section [Description] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8ad5fd9cf437afc3999697792850548e4e5a1435
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582895"
---
# <a name="form-configuration-file-description-section"></a>Section [Description] du fichier de configuration de formulaire
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La section **[Description]** répertorie toutes les propriétés du formulaire qui sont associées à des contrôles dans l’interface utilisateur du formulaire, ainsi que les attributs qui sont utilisés dans la localisation de l’écran. Le **MessageClass**, **Clsid**et entrées **DisplayName** , permettant d’identifier le nom de classe de message du formulaire, son GUID et nom d’affichage de la classe de message, respectivement, sont des entrées obligatoires permet de rechercher le formulaire dans la bibliothèque de formulaires . Les autres entrées sont facultatives. Le format de la section **[Description]** est la suivante : 
  
La section **[Description]** répertorie toutes les propriétés du formulaire qui sont associées à des contrôles dans l’interface utilisateur du formulaire, ainsi que les attributs qui sont utilisés dans la localisation de l’écran. Le **MessageClass**, **Clsid**et entrées **DisplayName** , permettant d’identifier le nom de classe de message du formulaire, son GUID et nom d’affichage de la classe de message, respectivement, sont des entrées obligatoires permet de rechercher le formulaire dans la bibliothèque de formulaires . Les autres entrées sont facultatives. Le format de la section **[Description]** est la suivante : 
  
 **[Description] MessageClass** =  _chaîne_
  
 **CLSID** =  _guid_
  
 **DisplayName** =  _displayedstring_
  
 **SmallIcon** =  _chemin d’accès_
  
 **LargeIcon** =  _chemin d’accès_
  
Entrées facultatives sont les suivants :
  
 **Catégorie** =  _affiche la chaîne_
  
 **Sous-catégorie** =  _affiche la chaîne_
  
 **Commentaire** =  _affiche la chaîne_
  
 **Propriétaire** =  _affiche la chaîne_
  
 **Numéro de** =  _affiche la chaîne_
  
 **Version** =  _entier_
  
 **Paramètres régionaux** =  _chaîne_
  
 **Masqué** =  _entier_
  
 **DesignerToolName** =  _chaîne_
  
 **DesignerToolGuid** =  _clsid_
  
 **DesignerRuntimeGuid** =  _clsid_
  
 **ComposeInFolder** =  _0 | 1_
  
 **ComposeCommand** =  _chaîne_
  
Les entrées de **catégorie** et une **sous-catégorie** sont utilisées par les programmes d’installation de l’écran pour configurer le classement par défaut des formulaires dans l’interface utilisateur de l’application cliente. Par exemple, une hiérarchie peut être configurée où « Help Desk » est la catégorie et « Software » et « Hardware » ont été les sous-catégories. Cette catégorisation puis utilisable par les applications de la visionneuse pour afficher les messages de manière plus organisée. Les entrées de **commentaire**, le **propriétaire**et **nombre** sont toutes les chaînes de commentaire qui apparaissent dans l’interface utilisateur de l’application cliente. Il s’agit des propriétés spécifiques du formulaire qui peuvent être utilisées à la discrétion du développeur du formulaire. Par exemple, l’entrée de **commentaire** peut être utilisée pour indiquer l’objectif de la forme, l’entrée de **propriétaire** est utilisée pour indiquer la personne ou l’organisation responsable de la maintenance du formulaire et le numéro utilisé pour effectuer le suivi de version différente du formulaire. **Commentaire** entrée, jusqu'à 10 lignes de commentaires peut être incluse. La première ligne de commentaires utilise le mot « Commentaire » comme clé, la deuxième ligne de commentaires utilise « Commentaires 1 » comme clé, et ainsi de suite par le biais de « Comment9 ». 
  
Les entrées **LargeIcon** et **SmallIcon** sont utilisées pour spécifier le chemin d’accès pour les ressources de l’icône utilisée pour afficher les icônes dans l’interface utilisateur de l’application cliente, en règle générale, il s’agit des lignes de tableau qui incluent la **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou les colonnes de propriétés **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Noms de fichiers icône peuvent être spécifiés en tant que chemins d’accès relatif au répertoire où le fichier de configuration de formulaire est installé. L’entrée de **Version** est utilisée pour indiquer le numéro de version du formulaire. **Paramètres régionaux** est l’identificateur de langue de trois lettres de la bibliothèque de formulaires de destination. Vous trouverez une liste des identificateurs suivants dans la _référence du programmeur Win32_.
  
L’entrée **masqué** indique si le formulaire doit être affiché dans l’interface utilisateur d’un fournisseur de bibliothèque de formulaires : 1 indique que le fichier est masqué et 0 indique que le formulaire est visible. Un exemple de fichier de configuration de formulaire est affiché suivant. 
  
L’entrée **ComposeInFolder** détermine si le formulaire est conçu pour être placé dans le dossier actif ou dans la boîte de réception de l’utilisateur lorsque l’utilisateur enregistre le message lors de sa composition : 1 indique que le formulaire doit être placé dans le dossier actif et 0 indique qu’il doit allez dans la boîte de réception. 
  
L’entrée **ComposeCommand** est la chaîne doit être placée dans l’application cliente de composition de menu. Si ce n’est pas spécifié, l’entrée **DisplayName** est utilisée. 
  
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


