---
title: MAPIFreeBuffer
description: Décrit la fonction MAPIFreeBuffer et fournit la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
ms.openlocfilehash: d91975f8fd7eb1b8d0b5acdda8784ad8914c3638
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818123"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Libère une mémoire tampon allouée avec un appel à la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) ou à la fonction [MAPIAllocateMore](mapiallocatemore.md) . 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Paramètres

 _lpBuffer_
  
> [in] Pointeur vers une mémoire tampon précédemment allouée. Si NULL est passé dans le paramètre _lpBuffer_ , **MAPIFreeBuffer** ne fait rien. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et libéré la mémoire demandée. **MAPIFreeBuffer** peut également retourner S_OK sur des emplacements déjà libérés ou si le bloc de mémoire n’est pas alloué avec **MAPIAllocateBuffer** et **MAPIAllocateMore**.
    
## <a name="remarks"></a>Remarques

En règle générale, lorsqu’une application cliente ou un fournisseur de services appelle [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), le système d’exploitation construit dans une mémoire tampon contiguë une ou plusieurs structures complexes avec plusieurs niveaux de pointeurs. Lorsqu’une fonction ou une méthode MAPI crée une mémoire tampon avec ce contenu, un client peut libérer ultérieurement toutes les structures contenues dans la mémoire tampon en passant à **MAPIFreeBuffer** le pointeur vers la mémoire tampon retournée par la fonction MAPI qui a créé la mémoire tampon. Pour qu’un fournisseur de services libère une mémoire tampon à l’aide de **MAPIFreeBuffer**, il doit passer le pointeur vers cette mémoire tampon retournée avec l’objet de support du fournisseur. 
  
L’appel à **MAPIFreeBuffer** pour libérer une mémoire tampon particulière doit être effectué dès qu’un client ou un fournisseur a terminé d’utiliser cette mémoire tampon. Le simple fait d’appeler la méthode [IMAPISession::Logoff](imapisession-logoff.md) à la fin d’une session MAPI ne libère pas automatiquement les mémoires tampons. 
  
Un client ou un fournisseur de services doit fonctionner en partant du principe que le pointeur passé dans  _lpBuffer_ n’est pas valide après un retour réussi de **MAPIFreeBuffer**. Si le pointeur indique un bloc de mémoire non alloué par le système de messagerie via **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou un bloc de mémoire libre, le comportement de **MAPIFreeBuffer** n’est pas défini. 
  
> [!NOTE]
> Le passage d’un pointeur Null à **MAPIFreeBuffer** simplifie et réduit le code de nettoyage de l’application, car **MAPIFreeBuffer** peut initialiser des pointeurs vers NULL, puis les libérer dans le code de nettoyage sans avoir à les tester en premier. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

