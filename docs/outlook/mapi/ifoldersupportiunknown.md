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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564170"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit des informations sur la prise en charge d’un dossier pour le partage.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |Fournisseur de banque de messages  <br/> |
|Identificateur de l’interface :  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtient des informations sur la prise en charge d’un dossier pour le partage.  <br/> |
   
## <a name="remarks"></a>Remarques

En règle générale, Microsoft Office Outlook requiert une MAPI magasin du fournisseur pour implémenter cette interface si le fournisseur souhaite partager un dossier. L’exception est le fournisseur de banque Exchange Server, qui peut partager des dossiers sans implémenter cette interface.
  
Un client peut demander un **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**. Si cette tentative réussit, appelez **IFolderSupport::GetSupportMask** et vérifiez le bit **FS_SUPPORTS_SHARING** à définir. 
  

