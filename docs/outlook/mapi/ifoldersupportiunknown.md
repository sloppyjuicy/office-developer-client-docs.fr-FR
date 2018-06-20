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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783712"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**S’applique à**: Outlook 
  
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
  

