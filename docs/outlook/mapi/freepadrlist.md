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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328034"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détruit une structure [ADRLIST](adrlist.md) et libère de la mémoire associée, y compris la mémoire allouée à tous les tableaux et structures membres. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Paramètres

 _padrlist_
  
> dans Pointeur vers la structure **ADRLIST** à détruire. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Dans le cadre de son implémentation de **FreePadrlist**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer toutes les entrées de la structure **ADRLIST** avant de libérer la structure complète. Par conséquent, toutes ces entrées doivent avoir suivi les règles d'allocation pour la structure [ADRLIST](adrlist.md) , à l'aide d'un appel [MAPIAllocateBuffer](mapiallocatebuffer.md) individuel pour chaque tableau et structure de membres. 
  
Pour plus d'informations sur l'allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIABFunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la méthode **FreePadrlist** pour libérer une structure ADRLIST qui a été conçue pour ajouter une adresse ponctuelle à un message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

