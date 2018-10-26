---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567852"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient des informations sur la prise en charge d’un dossier pour le partage.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Paramètres

 _pdwSupportMask_
  
> [out] Masque de bits indiquant si le dossier prend en charge le partage.
    
 **FS_NONE**
  
> Indique que le dossier ne prend pas en charge le partage.
    
 **FS_SUPPORTS_SHARING**
  
> Indique que le dossier prend en charge le partage.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi.
    

