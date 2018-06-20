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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783788"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**S’applique à**: Outlook 
  
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

