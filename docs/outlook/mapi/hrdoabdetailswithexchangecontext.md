---
title: HrDoABDetailsWithExchangeContext
description: Cet article décrit la fonction HrDoABDetailsWithExchangeContext et fournit la syntaxe et les paramètres.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
ms.openlocfilehash: 7a36ffe826dd4fe88b727d045cd7482a1cfdc128
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812375"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Garantit que la méthode **OpenEntry** est ouverte par le fournisseur de carnet d’adresses Exchange attendu. Cette fonction fonctionne de la même façon que [IAddrBook::D etails](iaddrbook-details.md), mais ouvre **l’entryID** à l’aide du carnet d’adresses Exchange identifié par le paramètre _pEmsmdbUID_. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
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
  
> Session **IMAPISession**. Il ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> Pointeur vers un **emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange utilisé par la fonction pour ouvrir l’identificateur d’entrée. Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée de fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et la fonction se comporte comme [IAddrBook::OpenEntry](iaddrbook-openentry.md). Si ce paramètre est NULL ou **mapIUID** zéro, cette fonction agit également exactement comme [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.
    
 _lpulUIParam_
  
> [out] Handle de la fenêtre parente de la boîte de dialogue.
    
 _lpfnDismiss_
  
> [in] Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** , ou NULL. Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de définition. MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ignore la boîte de dialogue d’adresse sans mode, informant un client qui appelle Details que la boîte de dialogue n’est plus active. 
    
 _lpvDismissContext_
  
> [in] Pointeur vers les informations de contexte à passer à la fonction **DISMISSMODELESS** pointée par le paramètre  _lpfnDismiss_ . Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue en incluant l’indicateur **DIALOG_SDI** dans le paramètre _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.
    
 _lpfButtonCallback_
  
> [in] Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON** . Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue détails. 
    
 _lpvButtonContext_
  
> [in] Pointeur vers les données utilisées comme paramètre pour la fonction spécifiée par le paramètre  _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible. Le paramètre  _lpszButtonText_ doit être NULL lorsqu’un bouton extensible n’est pas nécessaire. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type du texte pour le paramètre  _lpszButtonText_ . Les indicateurs suivants peuvent être définis : 
    
AB_TELL_DETAILS_CHANGE
  
> Indique que Details retourne TRUE si des modifications sont réellement apportées à l’adresse ; sinon, Details retourne FALSE.
    
DIALOG_MODAL
  
> Affiche la version modale de la boîte de dialogue d’adresse commune. Cet indicateur s’exclue mutuellement de DIALOG_SDI.
    
DIALOG_SDI
  
> Affiche la version sans mode de la boîte de dialogue d’adresse commune. Cet indicateur s’exclue mutuellement de DIALOG_MODAL.
    
MAPI_UNICODE
  
> Les chaînes passées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.
    

