---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 39a184f00ccf54d4fa4477bbdf3086f3e44bddb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576546"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Détruit une structure [ADRLIST](adrlist.md) et libère de la mémoire associée, y compris la mémoire allouée pour tous les tableaux membres et les structures. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Paramètres

 _padrlist_
  
> [in] Pointeur vers la structure **ADRLIST** destruction. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Dans le cadre de son implémentation de **FreePadrlist**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de chaque entrée dans la structure **ADRLIST** avant de libérer la structure complète. Par conséquent, toutes les entrées de ce type doivent avoir suivi les règles d’allocation de la structure [ADRLIST](adrlist.md) , à l’aide d’une personne [MAPIAllocateBuffer](mapiallocatebuffer.md) appeler pour chaque tableau de membres et de la structure. 
  
Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la méthode **FreePadrlist** pour libérer une structure ADRLIST qui a été conçue pour ajouter une adresse unique à un message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

