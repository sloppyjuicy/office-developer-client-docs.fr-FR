---
title: IExchangeModifyTableModifyTable
description: IExchangeModifyTableModifyTable met à jour un objet de table MAPI. Cet article décrit sa syntaxe, ses paramètres et fournit un exemple de code.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
ms.openlocfilehash: 87ffed62272372221e462df5c2f1741a829a031a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816373"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met à jour un objet de table MAPI.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Utilisez l’une des valeurs suivantes : 
    
0 (zéro)
  
> Utilisez la valeur du membre **ulRowFlags** de la structure [ROWENTRY](rowentry.md) . 
    
ACLTABLE_FREEBUSY
  
> Définit de nouveaux droits.
    
frightsFreeBusyDetailed
  
> Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage détaillé des nouveaux droits de disponibilité.
    
frightsFreeBusySimple
  
> Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage simple des nouveaux droits de disponibilité.
    
ROWLIST_REPLACE
  
> Remplacez toutes les lignes du tableau.
    
 _lpMods_
  
> [in] Pointe vers une structure [ROWLIST](rowlist.md) contenant les propriétés de l’objet table. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI utilise la méthode **IExchangeModifyTable::ModifyTable** pour réécrire une règle modifiée dans la table des règles. |
   
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

