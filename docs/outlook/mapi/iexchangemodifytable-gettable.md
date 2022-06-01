---
title: IExchangeModifyTableGetTable
description: IExchangeModifyTableGetTable renvoie un pointeur vers une interface pour un objet de table MAPI. Cet article décrit sa syntaxe, ses paramètres et un exemple de code.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
ms.openlocfilehash: 529be2d155362201790c230fcae71313a01c170a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816380"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur vers une interface pour un objet de table MAPI.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Réservé; doit être égal à 0 (zéro).
    
ACLTABLE_FREEBUSY
  
> Définit de nouveaux droits.
    
frightsFreeBusyDetailed
  
> Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage détaillé des nouveaux droits de disponibilité.
    
frightsFreeBusySimple
  
> Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage simple des nouveaux droits de disponibilité.
    
 _lppTable_
  
> [out] Pointe vers une interface [IMAPITable : IUnknown](imapitableiunknown.md) contenant l’objet table. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI utilise la méthode **IExchangeModifyTable::GetTable** pour obtenir une table de règles. |
   
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

