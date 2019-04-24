---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329007"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un signet à la position actuelle du tableau.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Paramètres

 _lpbkPosition_
  
> remarquer Pointeur vers la valeur de signet 32 bits renvoyée. Ce signet peut être passé ultérieurement dans un appel à la méthode [IMAPITable:: SeekRow](imapitable-seekrow.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> L'opération demandée n'a pas pu aboutir.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: CreateBookmark** marque une position de table en créant une valeur appelée signet. Un signet peut être utilisé pour revenir à la position identifiée par le signet. La position avec un signet est associée à l'objet sur cette ligne dans le tableau. 
  
Les signets ne sont pas pris en charge dans les tables de pièces jointes et les implémentations de table de pièces jointes de **CreateBookmark** renvoient MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

En raison du coût de la mémoire de maintien des positions de curseur avec des signets, limitez le nombre de signets que vous pouvez créer. Lorsque vous atteignez ce numéro, renvoyez MAPI_E_UNABLE_TO_COMPLETE de tous les appels suivants à **CreateBookmark**.
  
Parfois, un signet pointe vers une ligne qui n'est plus dans l'affichage tableau. Si un appelant utilise un signet de ce type, déplacez le curseur sur la ligne visible suivante et arrêtez-le. 
  
Lorsque l'appelant tente d'utiliser un signet pointant vers une ligne non visible, car il a été réduit, retournez MAPI_W_POSITION_CHANGED après avoir déplacé le signet. Vous pouvez repositionner le signet sur la ligne visible suivante à ce moment ou lorsque la réduction se produit dans la méthode **SetCollapseState** . Si vous déplacez le signet au moment de la réduction de la ligne, vous devez conserver un bit indiquant exactement la date de déplacement du signet: depuis sa dernière utilisation ou s'il n'a jamais été utilisé depuis sa création. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **CreateBookmark** alloue de la mémoire pour le signet qu'il crée. Libérez les ressources du signet en appelant la méthode [IMAPITable:: FreeBookmark](imapitable-freebookmark.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

