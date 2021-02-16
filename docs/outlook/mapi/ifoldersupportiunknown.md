---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415774"
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
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtient des informations sur la prise en charge d’un dossier pour le partage.  <br/> |
   
## <a name="remarks"></a>Remarques

En règle générale, Microsoft Office Outlook un fournisseur de magasin MAPI pour implémenter cette interface si le fournisseur souhaite partager un dossier. L’exception est le fournisseur Exchange Server store, qui peut partager des dossiers sans implémenter cette interface.
  
Un client peut interroger **[un IMAPIFolder](imapifolderimapicontainer.md)** pour **IFolderSupport**. Si cela réussit, appelez **IFolderSupport::GetSupportMask** et vérifiez la FS_SUPPORTS_SHARING **bit** à définir. 
  

