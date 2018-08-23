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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5e9135a52c15c18b70116aaf52e1ee63af413673
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563848"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée un signet à la position actuelle de la table.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Paramètres

 _lpbkPosition_
  
> [out] Pointeur vers la valeur renvoyée signet 32 bits. Ce signet peut ensuite être passé dans un appel à la méthode [IMAPITable::SeekRow](imapitable-seekrow.md) . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> L’opération demandée n’a pas pu aboutir.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::CreateBookmark** marque une position de la table en créant une valeur appelée un signet. Un signet peut être utilisé pour revenir à la position identifiée par le signet. La position du signet est associée à l’objet Row dans le tableau. 
  
Les signets ne sont pas pris en charge sur les tables des pièces jointes et les implémentations de tableau de pièce jointe de **CreateBookmark** retourner MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

En raison de la note de frais mémoire de maintenance de positions de curseur avec les signets, limiter le nombre de signets que vous pouvez créer. Lorsque ce nombre est atteint, renvoyer MAPI_E_UNABLE_TO_COMPLETE à partir de tous les appels suivants à **CreateBookmark**.
  
Parfois, un signet pointe vers une ligne qui n’est plus dans la vue table. Si un appelant utilise tel qu’un signet, déplacez le curseur sur la ligne suivante visible et s’y arrêter. 
  
Lorsque l’appelant essaie d’utiliser un signet qui pointe vers une ligne non visibles, car elle a été réduite, renvoie MAPI_W_POSITION_CHANGED après avoir déplacé le signet. Vous pouvez repositionner le signet à la ligne suivante visible à ce moment ou lorsque la réduction se produit dans la méthode **SetCollapseState** . Si vous déplacez le signet au moment de la ligne est réduite, vous devez conserver un peu du signet indiquant exactement quand le signet a été déplacé : depuis son dernier utiliser ou s’il n’a jamais été utilisé depuis sa création. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **CreateBookmark** alloue de la mémoire pour le signet qu’il crée. Libérer les ressources du signet en appelant la méthode [IMAPITable::FreeBookmark](imapitable-freebookmark.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

