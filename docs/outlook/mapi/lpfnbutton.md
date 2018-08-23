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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3b302de68f27e85c67430f82bd3e2c33009600e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591351"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel appels MAPI pour activer un contrôle bouton d’option dans une boîte de dialogue Carnet d’adresses. Ce bouton est généralement un bouton **Détails** . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction implémentée par :  <br/> |Fournisseurs de services  <br/> |
|Fonction appelée par :  <br/> |MAPI  <br/> |
   
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
  
> [in] Poignée de fenêtres parent pour toutes les boîtes de dialogue ou de windows qu'affiche cette fonction.
    
 _lpvContext_
  
> [in] Pointeur vers une valeur arbitraire transmis à la fonction de rappel lorsque MAPI il l’appelle. Cette valeur peut représenter une adresse de l’argument précision à l’application cliente. En règle générale, pour le code C++, _lpvContext_ représente un pointeur vers un objet C++. 
    
 _cbEntryID_
  
> [in] Taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpSelection_ . 
    
 _lpSelection_
  
> [in] Pointeur vers l’identificateur d’entrée définissant la sélection dans la boîte de dialogue.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Applications clientes appellent une fonction de rappel selon le prototype **LPFNBUTTON** permet de définir un bouton dans une boîte de dialogue Détails. Le client transmet un pointeur vers la fonction de rappel dans les appels à la méthode [IAddrBook::Details](iaddrbook-details.md) . 
  
Fournisseurs de services appellent une fonction de raccordement selon le prototype **LPFNBUTTON** permet de définir un bouton dans une boîte de dialogue Détails. Le fournisseur passe un pointeur vers cette fonction raccordement dans les appels à la méthode [IMAPISupport::Details](imapisupport-details.md) . 
  
Dans les deux cas, lorsque la boîte de dialogue s’affiche et l’utilisateur clique sur le bouton défini, appels MAPI **LPFNBUTTON**. 
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)

