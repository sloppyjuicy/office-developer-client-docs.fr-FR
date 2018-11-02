---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b801bdc06317738448a2205b60b94e1c9707d4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565906"
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

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Utilisez une des valeurs suivantes : 
    
0 (zéro)
  
> Utilisez la valeur du membre de la structure [ROWENTRY](rowentry.md) **ulRowFlags** . 
    
ACLTABLE_FREEBUSY
  
> Définit les nouveaux droits.
    
frightsFreeBusyDetailed
  
> Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage détaillé des nouveaux droits et de disponibilité.
    
frightsFreeBusySimple
  
> Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage simple de nouveaux droits et de disponibilité.
    
ROWLIST_REPLACE
  
> Remplacer toutes les lignes dans le tableau.
    
 _lpMods_
  
> [in] Pointe vers une structure [ROWLIST](rowlist.md) contenant les propriétés de l’objet table. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI utilise la méthode **IExchangeModifyTable::ModifyTable** pour écrire une règle modifiée dans la table des règles.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

