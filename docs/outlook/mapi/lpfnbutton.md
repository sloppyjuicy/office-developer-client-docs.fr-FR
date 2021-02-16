---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431511"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel que MAPI appelle pour activer un contrôle de bouton facultatif dans une boîte de dialogue de carnet d’adresses. Ce bouton est généralement un **bouton Détails.** 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction définie implémentée par :  <br/> |Fournisseurs de services  <br/> |
|Fonction définie appelée par :  <br/> |MAPI  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle of the parent windows for any dialog boxes or windows this function displays.
    
 _lpvContext_
  
> [in] Pointeur vers une valeur arbitraire transmise à la fonction de rappel lorsque MAPI l’appelle. Cette valeur peut représenter une adresse significative pour l’application cliente. En règle générale, pour le code C++,  _lpvContext_ représente un pointeur vers un objet C++. 
    
 _cbEntryID_
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par _le paramètre lpSelection._ 
    
 _lpSelection_
  
> [in] Pointeur vers l’identificateur d’entrée définissant la sélection dans la boîte de dialogue.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent une fonction de rappel basée sur le prototype **LPFNBUTTON** pour définir un bouton dans une boîte de dialogue de détails. Le client transmet un pointeur vers la fonction de rappel dans les appels à la méthode [IAddrBook::D etails.](iaddrbook-details.md) 
  
Les fournisseurs de services appellent une fonction hook basée sur le prototype **LPFNBUTTON** pour définir un bouton dans une boîte de dialogue de détails. Le fournisseur transmet un pointeur vers cette fonction hook dans les appels à la méthode [IMAPISupport::D etails.](imapisupport-details.md) 
  
Dans les deux cas, lorsque la boîte de dialogue s’affiche et que l’utilisateur choisit le bouton défini, MAPI appelle **LPFNBUTTON**. 
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)

