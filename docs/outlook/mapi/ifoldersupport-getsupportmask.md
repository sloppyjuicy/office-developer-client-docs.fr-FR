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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783682"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**S’applique à**: Outlook 
  
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
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi.
    

