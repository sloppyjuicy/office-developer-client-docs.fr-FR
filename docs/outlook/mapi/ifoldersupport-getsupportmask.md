---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f337f93393766d6a456d5659b8f1cee13d23a299
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600959"
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
    

