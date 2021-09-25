---
title: MAPIFreeBuffer
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3b952e6a62af99f9aa1a1afd0ec96102e54318c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556076"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Libère une mémoire tampon allouée avec un appel à la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore.](mapiallocatemore.md) 
  
|||
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
  
> [in] Pointeur vers une mémoire tampon précédemment allouée. Si NULL est transmis dans le  _paramètre lpBuffer,_ **MAPIFreeBuffer** ne fait rien. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et libéré la mémoire demandée. **MAPIFreeBuffer** peut également renvoyer des S_OK sur des emplacements déjà libérés ou si le bloc de mémoire n’est pas alloué avec **MAPIAllocateBuffer** et **MAPIAllocateMore**.
    
## <a name="remarks"></a>Remarques

En règle générale, lorsqu’une application cliente ou un fournisseur de services appelle [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), le système d’exploitation construit dans une mémoire tampon contiguë une ou plusieurs structures complexes avec plusieurs niveaux de pointeurs. Lorsqu’une fonction ou une méthode MAPI crée une mémoire tampon avec ce contenu, un client peut ensuite libérer toutes les structures contenues dans la mémoire tampon en passant à **MAPIFreeBuffer** le pointeur vers la mémoire tampon renvoyée par la fonction MAPI qui a créé la mémoire tampon. Pour qu’un fournisseur de services libère une mémoire tampon à l’aide de **MAPIFreeBuffer,** il doit transmettre le pointeur à cette mémoire tampon renvoyée avec l’objet de support du fournisseur. 
  
L’appel **à MAPIFreeBuffer** pour libérer une mémoire tampon particulière doit être effectué dès qu’un client ou un fournisseur a terminé d’utiliser cette mémoire tampon. Le simple fait d’appeler la méthode [IMAPISession::Logoff](imapisession-logoff.md) à la fin d’une session MAPI ne libère pas automatiquement les mémoires tampons. 
  
Un client ou un fournisseur de services doit fonctionner sur l’hypothèse que le pointeur passé dans  _lpBuffer_ n’est pas valide après un retour réussi de **MAPIFreeBuffer**. Si le pointeur indique soit un bloc de mémoire non alloué par le système de messagerie via **MAPIAllocateBuffer** ou **MAPIAllocateMore,** soit un bloc de mémoire libre, le comportement de **MAPIFreeBuffer** n’est pas indéfini. 
  
> [!NOTE]
> La transmission d’un pointeur null à **MAPIFreeBuffer** simplifie et simplifie le code de nettoyage de l’application, car **MAPIFreeBuffer** peut initialiser les pointeurs sur NULL, puis les libérer dans le code de nettoyage sans avoir à les tester au premier abord. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

