---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 22aad12010a4f367e18443d8c0831c6262cc37fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784767"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**S’applique à**: Outlook 
  
Libère une mémoire tampon alloué avec un appel à la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Paramètres

 _lpBuffer_
  
> [in] Pointeur vers un tampon de mémoire allouée précédemment. Si NULL est indiqué dans le paramètre _lpBuffer_ , **MAPIFreeBuffer** est sans effet. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et libérer de la mémoire requise. **MAPIFreeBuffer** peut aussi renvoyer S_OK dans des emplacements déjà libérés ou le bloc de mémoire non allouée avec **MAPIAllocateBuffer** et **MAPIAllocateMore**.
    
## <a name="remarks"></a>Remarques

En règle générale, lorsqu’une application cliente ou un fournisseur de services appelle [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), les constructions de système d’exploitation dans une mémoire contiguë tampon un ou plusieurs des structures complexes avec plusieurs niveaux de pointeurs. Lorsqu’une fonction MAPI ou méthode crée un tampon avec ce type de contenu, un client peut libérer ultérieurement toutes les structures contenues dans la mémoire tampon, en passant à **MAPIFreeBuffer** le pointeur vers la mémoire tampon retournée par la fonction MAPI qui a créé la mémoire tampon. Pour un fournisseur de service libérer de l’une à l’aide de **MAPIFreeBuffer**de mémoire tampon, il doit passer le pointeur à cette mémoire tampon renvoyée avec l’objet de prise en charge du fournisseur. 
  
L’appel à **MAPIFreeBuffer** pour libérer un tampon particulier doit être effectuée dès qu’un client ou fournisseur est terminé, à l’aide de cette mémoire tampon. Simplement en appelant la méthode [IMAPISession::Logoff](imapisession-logoff.md) à la fin d’une session MAPI n’annule pas automatiquement les mémoires tampon. 
  
Un client ou fournisseur de services doit fonctionner sur l’hypothèse que le pointeur passé _lpBuffer_ est non valide après le retour à partir de **MAPIFreeBuffer**réussi. Si le pointeur indique un bloc de mémoire non alloué par le système de messagerie via **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou un bloc de mémoire disponible, le comportement de **MAPIFreeBuffer** est indéfini. 
  
> [!NOTE]
> Passer un pointeur null à **MAPIFreeBuffer** rend application nettoyage code plus simple et plus petits car **MAPIFreeBuffer** peut initialiser des pointeurs NULL et les libérer dans le code de nettoyage sans avoir à les tester tout d’abord. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

