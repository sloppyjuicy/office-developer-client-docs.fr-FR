---
title: IExchangeModifyTableModifyTable
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 460ec105fea740a81fdb8102b12d19f7bb875b8c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613904"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met à jour un objet table MAPI.
  
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
  
> Utilisez la valeur du **membre ulRowFlags** de la structure [ROWENTRY.](rowentry.md) 
    
ACLTABLE_FREEBUSY
  
> Définit de nouveaux droits.
    
frightsFreeBusyDetailed
  
> Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage détaillé des nouveaux droits de libre/occupé.
    
frightsFreeBusySimple
  
> Lorsque ACLTABLE_FREEBUSY est passé, fournit un affichage simple des nouveaux droits de libre/occupé.
    
ROWLIST_REPLACE
  
> Remplacez toutes les lignes du tableau.
    
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

