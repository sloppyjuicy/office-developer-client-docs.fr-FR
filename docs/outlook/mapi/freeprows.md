---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0686cee9bf6fa47332f75f99e1d2a2d35cb7e7fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578023"
---
# <a name="freeprows"></a>FreeProws

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Détruit une structure [SRowSet](srowset.md) et libère de la mémoire associée, y compris la mémoire allouée pour tous les tableaux membres et les structures. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Paramètres

 _PROWS_
  
> [in] Pointeur vers la structure **SRowSet** destruction. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Dans le cadre de son implémentation de **FreeProws**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de chaque entrée dans la structure **SRowSet** avant de libérer la structure complète. Par conséquent, toutes les entrées de ce type doivent avoir suivi les règles d’allocation de la structure [SRowSet](srowset.md) , à l’aide d’une personne [MAPIAllocateBuffer](mapiallocatebuffer.md) appeler pour chaque tableau de membres et de la structure. 
  
Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la méthode **FreeProws** pour libérer une structure SRowSet contenant les lignes de la table en cours de traitement.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

