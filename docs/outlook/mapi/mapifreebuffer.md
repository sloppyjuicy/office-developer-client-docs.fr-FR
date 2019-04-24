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
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346661"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Libère une mémoire tampon allouée à l'aide d'un appel à la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) ou à la fonction [MAPIAllocateMore](mapiallocatemore.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Paramètres

 _lpBuffer_
  
> dans Pointeur vers une mémoire tampon de mémoire allouée précédemment. Si NULL est passé dans le paramètre _lpBuffer_ , **MAPIFreeBuffer** n'a aucun effet. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a libéré la mémoire demandée. **MAPIFreeBuffer** peut également renvoyer S_OK sur des emplacements déjà libérés ou si le bloc de mémoire n'est pas alloué avec **MAPIAllocateBuffer** et **MAPIAllocateMore**.
    
## <a name="remarks"></a>Remarques

En règle générale, lorsqu'une application cliente ou un fournisseur de services appelle [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), le système d'exploitation construit dans un tampon de mémoire contigu une ou plusieurs structures complexes avec plusieurs niveaux de pointeurs. Lorsqu'une fonction ou méthode MAPI crée une mémoire tampon avec un tel contenu, un client peut libérer ultérieurement toutes les structures contenues dans la mémoire tampon en transmettant à **MAPIFreeBuffer** le pointeur vers la mémoire tampon renvoyée par la fonction MAPI qui a créé la mémoire tampon. Pour qu'un fournisseur de services libère une mémoire tampon à l'aide de **MAPIFreeBuffer**, il doit transmettre le pointeur à ce tampon renvoyé avec l'objet de support du fournisseur. 
  
L'appel à **MAPIFreeBuffer** pour libérer une mémoire tampon particulière doit être effectué dès qu'un client ou un fournisseur a terminé d'utiliser cette mémoire tampon. Le simple fait d'appeler la méthode [IMAPISession:: Logoff](imapisession-logoff.md) à la fin d'une session MAPI ne libère pas automatiquement les mémoires tampons de mémoire. 
  
Un client ou un fournisseur de services doit agir en supposant que le pointeur transmis dans _lpBuffer_ n'est pas valide après un retour de **MAPIFreeBuffer**. Si le pointeur indique un bloc de mémoire qui n'est pas alloué par le système de messagerie via **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou un bloc de mémoire libre, le comportement de **MAPIFreeBuffer** n'est pas défini. 
  
> [!NOTE]
> Le passage d'un pointeur null à **MAPIFreeBuffer** rend le code de nettoyage d'application plus simple et plus petit car **MAPIFreeBuffer** peut initialiser des pointeurs vers des valeurs NULL, puis les libérer dans le code de nettoyage sans avoir à les tester d'abord. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

