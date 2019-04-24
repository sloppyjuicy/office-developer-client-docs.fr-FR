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
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351386"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations sur la prise en charge du partage par un dossier.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |Fournisseur de banque de messages  <br/> |
|Identificateur de l'interface:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtient des informations sur la prise en charge d'un dossier pour le partage.  <br/> |
   
## <a name="remarks"></a>Remarques

En règle générale, Microsoft Office Outlook requiert un fournisseur de banque MAPI pour implémenter cette interface si le fournisseur souhaite partager un dossier. L'exception est le fournisseur de banque d'Exchange Server, qui peut partager des dossiers sans mettre en œuvre cette interface.
  
Un client peut interroger un **[IMAPIFolder](imapifolderimapicontainer.md)** pour **IFolderSupport**. Si cette opération réussit, appelez **IFolderSupport:: GetSupportMask** et vérifiez que le bit **FS_SUPPORTS_SHARING** doit être défini. 
  

