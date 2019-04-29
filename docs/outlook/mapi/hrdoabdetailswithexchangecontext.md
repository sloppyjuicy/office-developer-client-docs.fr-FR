---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421367"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Garantit que la méthode **OpenEntry** est ouverte par le fournisseur de carnet d'adresses Exchange attendu. Cette fonction fonctionne de la même manière que [IAddrBook::D etails](iaddrbook-details.md), mais il ouvre la propriété **entryID** à l'aide du carnet d'adresses Exchange identifié par le paramètre _pEmsmdbUID_ . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a>Paramètres

 _pmsess_
  
> Le **IMAPISession**connecté. Il ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> Pointeur vers un **emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnets d'adresses Exchange utilisé par la fonction pour ouvrir l'identificateur d'entrée. Si l'identificateur d'entrée entrante n'est pas un identificateur d'entrée de fournisseur de carnet d'adresses Exchange, ce paramètre est ignoré et la fonction se comporte comme [IAddrBook:: OpenEntry](iaddrbook-openentry.md). Si ce paramètre a la valeur NULL ou a la valeur zéro **MAPIUID**, cette fonction agit également exactement comme [IAddrBook:: OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée. Il ne peut pas être NULL.
    
 _lpulUIParam_
  
> remarquer Handle de la fenêtre parente de la boîte de dialogue.
    
 _lpfnDismiss_
  
> dans Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** , ou valeur null. Ce membre s'applique uniquement à la version non modale de la boîte de dialogue, comme indiqué par l'indicateur DIALOG_SDI défini. MAPI appelle la fonction **DISMISSMODELESS** lorsque l'utilisateur fait disparaître la boîte de dialogue d'adresses non modale, en informant un client qui appelle les détails que la boîte de dialogue n'est plus active. 
    
 _lpvDismissContext_
  
> dans Pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** vers laquelle pointe le paramètre _lpfnDismiss_ . Ce paramètre s'applique uniquement à la version non modale de la boîte de dialogue en incluant l'indicateur **DIALOG_SDI** dans le paramètre _ulFlags_ . 
    
 _cbEntryID_
  
> dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.
    
 _lpfButtonCallback_
  
> dans Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON** . Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue détails. 
    
 _lpvButtonContext_
  
> dans Pointeur vers les données qui ont été utilisées comme paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> dans Pointeur vers une chaîne qui contient le texte à appliquer au bouton ajouté, si ce bouton est extensible. Le paramètre _lpszButtonText_ doit être null lorsqu'un bouton extensible n'est pas nécessaire. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de texte pour le paramètre _lpszButtonText_ . Les indicateurs suivants peuvent être définis: 
    
AB_TELL_DETAILS_CHANGE
  
> Indique que les détails renvoient la valeur TRUE si les modifications sont réellement apportées à l'adresse; dans le cas contraire, la méthode Details renvoie FALSe.
    
DIALOG_MODAL
  
> Affiche la version modale de la boîte de dialogue adresse commune. Cet indicateur est mutuellement exclusif avec DIALOG_SDI.
    
DIALOG_SDI
  
> Affiche la version non modale de la boîte de dialogue adresse commune. Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.
    
MAPI_UNICODE
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    

