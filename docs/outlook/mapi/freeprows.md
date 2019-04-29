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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438819"
---
# <a name="freeprows"></a>FreeProws

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détruit une structure [SRowSet](srowset.md) et libère de la mémoire associée, y compris la mémoire allouée à tous les tableaux et structures membres. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Paramètres

 _PROWS_
  
> dans Pointeur vers la structure **SRowSet** à détruire. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Dans le cadre de son implémentation de **FreeProws**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer toutes les entrées de la structure **SRowSet** avant de libérer la structure complète. Par conséquent, toutes ces entrées doivent avoir suivi les règles d'allocation pour la structure [SRowSet](srowset.md) , à l'aide d'un appel [MAPIAllocateBuffer](mapiallocatebuffer.md) individuel pour chaque tableau et structure de membres. 
  
Pour plus d'informations sur l'allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la méthode **FreeProws** pour libérer une structure SRowSet contenant les lignes de la table en cours de traitement.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

