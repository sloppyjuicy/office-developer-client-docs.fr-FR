---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8b5aa71e81c8bc73b73d6aa3586ff81466e1e6e3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773774"
---
# <a name="freeprows"></a>FreeProws

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détruit une structure [SRowSet](srowset.md) et libère la mémoire associée, y compris la mémoire allouée à tous les tableaux et structures membres. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Paramètres

 _prows_
  
> [in] Pointeur vers la structure **SRowSet** à détruire. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Dans le cadre de son implémentation de **FreeProws**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer chaque entrée dans la structure **SRowSet** avant de libérer la structure complète. Par conséquent, toutes ces entrées doivent avoir suivi les règles d’allocation pour la structure [SRowSet](srowset.md) , à l’aide d’un appel [MAPIAllocateBuffer](mapiallocatebuffer.md) individuel pour chaque matrice et structure de membre. 
  
Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la **méthode FreeProws** pour libérer une structure SRowSet contenant des lignes de la table en cours de traitement. |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

