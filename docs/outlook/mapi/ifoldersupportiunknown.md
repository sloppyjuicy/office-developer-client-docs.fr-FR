---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d473fa09fd42d6ec4583e18f3698400ead80b54e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779937"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations sur la prise en charge d’un dossier pour le partage.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |Fournisseur de magasin de messages  <br/> |
|Identificateur d’interface :  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtient des informations sur la prise en charge d’un dossier pour le partage. |
   
## <a name="remarks"></a>Remarques

En règle générale, Microsoft Office Outlook nécessite un fournisseur de magasin MAPI pour implémenter cette interface si le fournisseur souhaite partager un dossier. L’exception est le fournisseur Exchange Server store, qui peut partager des dossiers sans implémenter cette interface.
  
Un client peut interroger **[un IMAPIFolder](imapifolderimapicontainer.md)** pour **IFolderSupport**. Si cela réussit, appelez **IFolderSupport::GetSupportMask** et vérifiez la **FS_SUPPORTS_SHARING bit à** définir. 
  

