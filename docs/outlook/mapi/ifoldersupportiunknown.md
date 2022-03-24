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
description: Fournit des informations sur la prise en charge d’un dossier pour le partage. En règle générale, Outlook un fournisseur de magasin MAPI implémente cette interface pour partager un dossier.
ms.openlocfilehash: ac138682b846647162162a9775334740c59f44a5
ms.sourcegitcommit: c68b7b7f98b3ff9e6de37ee5877adcad2e5e71d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63742136"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations sur la prise en charge d’un dossier pour le partage.
  
|Propriété |Valeur |
|:-----|:-----|
|Fourni par :  <br/> |Fournisseur de magasin de messages  <br/> |
|Identificateur d’interface :  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Propriété |Valeur |
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtient des informations sur la prise en charge d’un dossier pour le partage. |
   
## <a name="remarks"></a>Remarques

En règle générale, Microsoft Office Outlook nécessite un fournisseur de magasin MAPI pour implémenter cette interface si le fournisseur souhaite partager un dossier. L’exception est le fournisseur Exchange Server store, qui peut partager des dossiers sans implémenter cette interface.
  
Un client peut interroger **[un IMAPIFolder](imapifolderimapicontainer.md)** pour **IFolderSupport**. Si cela réussit, appelez **IFolderSupport::GetSupportMask** et vérifiez la **FS_SUPPORTS_SHARING bit à** définir. 
  

