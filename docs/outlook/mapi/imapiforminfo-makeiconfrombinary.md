---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 813c76d2c4d81dd50760fc356c2af6f8cc41054e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567584"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une icône à partir de l’une des propriétés d’icône d’un formulaire.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Paramètres

 _nPropID_
  
> [in] Identificateur de propriété pour une propriété d’icône.
    
 _phicon_
  
> [out] Pointeur vers l’icône renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormInfo::MakeIconFromBinary** pour créer une icône à partir de l’une des propriétés d’icône d’un formulaire. Dans le  _paramètre nPropID,_ **MakeIconFromBinary** prend l’identificateur de propriété d’une des propriétés d’icône d’un formulaire. À l’aide de cet identificateur de propriété, il crée une icône qui peut être affichée dans les vues de tableau qui incluent des colonnes de propriété pour les icônes. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

