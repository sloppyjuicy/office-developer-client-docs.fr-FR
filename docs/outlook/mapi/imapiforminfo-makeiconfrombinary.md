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
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405113"
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

Les applications clientes appellent la méthode **IMAPIFormInfo::MakeIconFromBinary** pour créer une icône à partir de l’une des propriétés d’icône d’un formulaire. Dans le  _paramètre nPropID,_ **MakeIconFromBinary** prend l’identificateur de propriété de l’une des propriétés d’icône d’un formulaire. À l’aide de cet identificateur de propriété, il crée une icône qui peut être affichée dans les vues de tableau qui incluent des colonnes de propriété pour les icônes. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

