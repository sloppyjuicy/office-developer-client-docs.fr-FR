---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 30f55044327eecee3ab0d8ee2509d7132ab6e8ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570127"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée une icône à partir d’une des propriétés d’icône d’un formulaire.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Paramètres

 _nPropID_
  
> [in] Un identificateur de propriété pour une propriété d’icône.
    
 _phicon_
  
> [out] Pointeur vers l’icône renvoyée.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Applications clientes appellent la méthode **IMAPIFormInfo::MakeIconFromBinary** pour créer une icône de l’une des propriétés d’icône d’un formulaire. Dans le paramètre _nPropID_ , **MakeIconFromBinary** est l’identificateur de propriété d’une des propriétés d’icône d’un formulaire. À l’aide de l’identificateur de cette propriété, il crée une icône qui peut être affichée dans les tableaux qui contiennent des colonnes de propriété pour les icônes. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

