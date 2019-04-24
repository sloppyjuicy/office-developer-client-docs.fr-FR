---
title: Section [Description] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320985"
---
# <a name="form-configuration-file-description-section"></a>Section [Description] du fichier de configuration de formulaire
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Description]** répertorie toutes les propriétés du formulaire qui sont associées aux contrôles dans l'interface utilisateur du formulaire, ainsi que les attributs utilisés lors de la recherche du formulaire. Les entrées **MessageClass**, **CLSID**et **DisplayName** , qui identifient le nom de la classe de message, son GUID et le nom d'affichage de la classe de message, respectivement, sont des entrées requises pour localiser le formulaire dans la bibliothèque de formulaires. . Les entrées restantes sont facultatives. Le format de la section **[Description]** est le suivant: 
  
La section **[Description]** répertorie toutes les propriétés du formulaire qui sont associées aux contrôles dans l'interface utilisateur du formulaire, ainsi que les attributs utilisés lors de la recherche du formulaire. Les entrées **MessageClass**, **CLSID**et **DisplayName** , qui identifient le nom de la classe de message, son GUID et le nom d'affichage de la classe de message, respectivement, sont des entrées requises pour localiser le formulaire dans la bibliothèque de formulaires. . Les entrées restantes sont facultatives. Le format de la section **[Description]** est le suivant: 
  
 **Description ** =  _Chaîne_ MessageClass
  
 **** =  _GUID_ CLSID
  
 **DisplayName** =  _displayedstring_
  
 **** =  _Chemin d'accès_ SmallIcon
  
 **** =  _Chemin d'accès_ LargeIcon
  
Les entrées facultatives sont les suivantes:
  
 **** =  _Chaîne affichée_ sous la catégorie
  
 **** =  _Chaîne affichée sous_ -catégorie
  
 **** =  _Chaîne affichée_ de commentaire
  
 **** =  _Chaîne affichée_ par le propriétaire
  
 **** =  _Chaîne affichée_ en nombre
  
 **** =  _Entier_ de version
  
 **Chaîne de paramètres régionaux**__  =  
  
 **** =  _Entier_ masqué
  
 **** =  _Chaîne_ DesignerToolName
  
 **** =  _CLSID_ DesignerToolGuid
  
 **** =  _CLSID_ DesignerRuntimeGuid
  
 **ComposeInFolder** =  _0 | 1_
  
 **** =  _Chaîne_ ComposeCommand
  
Les entrées de **catégorie** et de **sous-catégorie** sont utilisées par les programmes d'installation de formulaire pour configurer la catégorisation par défaut des formulaires dans l'interface utilisateur de l'application cliente. Par exemple, une hiérarchie peut être configurée où «support technique» est la catégorie et «logiciel» et «matériel» étaient les sous-catégories. Cette catégorisation peut ensuite être utilisée par les applications de la visionneuse pour afficher les messages d'une manière plus organisée. Les entrées de **Commentaire**, de **propriétaire**et de **numéro** sont toutes des chaînes de commentaires qui apparaissent dans l'interface utilisateur de l'application cliente. Il s'agit de propriétés spécifiques qui peuvent être utilisées à la discrétion du développeur de formulaires. Par exemple, l'entrée de **Commentaire** peut être utilisée pour indiquer l'objectif du formulaire, l'entrée de **propriétaire** utilisée pour indiquer la personne ou l'organisation chargée de la gestion du formulaire, ainsi que le numéro utilisé pour suivre différentes versions du formulaire. Pour l'entrée de **Commentaire** , jusqu'à dix lignes de commentaires peuvent être incluses. La première ligne de commentaires utilise le mot «commentaire» comme clé, la deuxième ligne de commentaires utilise «Comment1» comme clé, et ainsi de suite par «Comment9». 
  
Les entrées **LargeIcon** et **SmallIcon** sont utilisées pour spécifier le chemin d'accès aux ressources d'icône utilisées pour afficher les icônes dans l'interface utilisateur de l'application cliente, en règle générale, il s'agit des lignes de tableau qui incluent le **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)). ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Les noms de fichiers d'icônes peuvent être spécifiés sous forme de chemins d'accès par rapport au répertoire dans lequel le fichier de configuration du formulaire est installé. L'entrée de **version** est utilisée pour indiquer le numéro de version du formulaire. **Paramètres régionaux** est l'identificateur de langue à trois lettres de la bibliothèque de formulaires de destination. Une liste de ces identificateurs est disponible dans le _Guide de référence du programmeUr Win32_.
  
L' **** entrée masquée indique si le formulaire doit être affiché dans l'interface utilisateur d'un fournisseur de bibliothèque de formulaires: 1 indique que le fichier est masqué et 0 indique que le formulaire est visible. Un exemple de fichier de configuration de formulaire est illustré ci-dessous. 
  
L'entrée **ComposeInFolder** contrôle si le formulaire est conçu pour être placé dans le dossier actif ou dans la boîte de réception de l'utilisateur lorsque l'utilisateur enregistre le message pendant qu'il le compose: 1 indique que le formulaire doit se trouver dans le dossier actif et 0 indique qu'il doit Accédez à la boîte de réception. 
  
L'entrée **ComposeCommand** est la chaîne à placer dans le menu de composition de l'application cliente. Si ce n'est pas spécifié, l'entrée **DisplayName** est utilisée. 
  
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


