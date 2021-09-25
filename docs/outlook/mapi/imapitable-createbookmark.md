---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e3605dc630b6a7bcff46aa3a038d4a4ec7a1f114
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600966"
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
  
> [out] Pointeur vers la valeur de signet 32 bits renvoyée. Ce signet peut ensuite être transmis dans un appel à la [méthode IMAPITable::SeekRow.](imapitable-seekrow.md) 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> L’opération demandée n’a pas pu être achevée.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::CreateBookmark** marque une position de tableau en créant une valeur appelée signet. Un signet peut être utilisé pour revenir à la position identifiée par le signet. La position avec signet est associée à l’objet à cette ligne du tableau. 
  
Les signets ne sont pas pris en charge sur les tables de pièces jointes et les implémentations de table de pièces jointes **de CreateBookmark** MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

En raison de la dépense de mémoire de la gestion des positions du curseur avec des signets, limitez le nombre de signets que vous pouvez créer. Lorsque vous atteignez ce nombre, renvoyez MAPI_E_UNABLE_TO_COMPLETE de tous les appels suivants **à CreateBookmark**.
  
Parfois, un signet pointe vers une ligne qui n’est plus dans l’affichage Tableau. Si un appelant utilise un signet de ce type, déplacez le curseur sur la ligne visible suivante et arrêtez-le. 
  
Lorsque l’appelant tente d’utiliser un signet qui pointe vers une ligne nonvisible car elle a été réduire, renvoyer MAPI_W_POSITION_CHANGED après le déplacement du signet. Vous pouvez repositionner le signet sur la ligne visible suivante à ce moment-là ou lorsque la réduction se produit dans la **méthode SetCollapseState.** Si vous déplacez le signet au moment où la ligne est réduire, vous devez conserver un bit dans le signet qui indique exactement quand le signet a été déplacé : depuis sa dernière utilisation ou s’il n’a jamais été utilisé depuis sa création. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **CreateBookmark alloue** de la mémoire pour le signet qu’il crée. Libérez les ressources du signet en appelant la [méthode IMAPITable::FreeBookmark.](imapitable-freebookmark.md) 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

