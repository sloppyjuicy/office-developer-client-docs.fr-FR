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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350833"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient des informations sur la prise en charge d'un dossier pour le partage.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Paramètres

 _pdwSupportMask_
  
> remarquer Masque de masque indiquant si le dossier prend en charge le partage.
    
 **FS_NONE**
  
> Indique que le dossier ne prend pas en charge le partage.
    
 **FS_SUPPORTS_SHARING**
  
> Indique que le dossier prend en charge le partage.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi.
    

