---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: db2b937d39dac521caa60e2f1e9f9664384b8a23
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778893"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détruit une structure [ADRLIST](adrlist.md) et libère la mémoire associée, y compris la mémoire allouée à tous les tableaux et structures membres. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Paramètres

 _padrlist_
  
> [in] Pointeur vers la structure **ADRLIST** à détruire. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Dans le cadre de son implémentation de **FreePadrlist**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer chaque entrée dans la structure **ADRLIST** avant de libérer la structure complète. Par conséquent, toutes ces entrées doivent avoir suivi les règles d’allocation pour la structure [ADRLIST](adrlist.md) , à l’aide d’un appel [MAPIAllocateBuffer](mapiallocatebuffer.md) individuel pour chaque matrice et structure de membre. 
  
Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la **méthode FreePadrlist** pour libérer une structure ADRLIST qui a été conçue pour ajouter une adresse à un message. |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

