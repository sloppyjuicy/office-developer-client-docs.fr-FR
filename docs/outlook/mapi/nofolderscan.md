---
title: NoFolderScan
description: Décrit les informations de propriété et les remarques pour NoFolderScan, qui spécifie si Microsoft Office Outlook devez analyser les dossiers Contacts sur un magasin.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
ms.openlocfilehash: 68e98b7f5a44d84f84d274273d9e33269f909b50
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852690"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si Microsoft Office Outlook devez analyser les dossiers Contacts dans un magasin.
  
## <a name="quick-info"></a>Informations rapides

|Propriété|Valeur|
|:-----|:-----|
|Exposé sur :  <br/> |[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par :  <br/> |Fournisseur du Store  <br/> |
|Accessible par :  <br/> |Outlook et d’autres clients  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Type d’accès :  <br/> |En lecture seule ou en lecture/écriture en fonction du fournisseur de magasins  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et retourner une étiquette de propriété valide pour l’une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété pour l’une de ces propriétés est passée à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasin doit également retourner la valeur de propriété correcte. Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel [d’IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre  _d’entrée lppPropNames_ :
  
|Propriété|Valeur|
|:-----|:-----|
|lpGuid :  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L"NoFolderScan »  <br/> |
   
Cette propriété permet aux fournisseurs de magasin de spécifier de Outlook de ne pas analyser les dossiers Contacts dans le magasin afin d’éviter une dégradation des performances. Il est utilisé dans les opérations de fusion et publipostage au cours desquelles Outlook vérifie la présence et la valeur de cette propriété avant de lancer l’analyse.
  
Par défaut, cette propriété n’est pas exposée sur un magasin, ce qui signifie que Outlook pouvez analyser le dossier Contacts sur le magasin. Si la propriété est exposée, voici les valeurs possibles :
  
- Zéro (0) : Outlook pouvez effectuer l’analyse.
    
- Valeur différente de zéro : Outlook ne doit pas analyser les dossiers Contacts sur le magasin.
    

