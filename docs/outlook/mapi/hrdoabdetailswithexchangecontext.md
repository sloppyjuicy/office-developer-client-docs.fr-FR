---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e041597a01774fcdda3d99532bf5b062acdd46ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584533"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Garantit que la **méthode OpenEntry** est ouverte par le fournisseur de carnet d’adresses Exchange attendu. Cette fonction fonctionne de la même manière que [IAddrBook::D etails,](iaddrbook-details.md)mais ouvre **l’entryID** à l’aide du carnet d’adresses Exchange identifié par le paramètre _pEmsmdbUID._ 
  
|||
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
  
> **L’IMAPISession** connecté. Elle ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> Pointeur vers **un élément emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange utilisé par la fonction pour ouvrir l’identificateur d’entrée. Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée de fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et la fonction se comporte comme [IAddrBook::OpenEntry](iaddrbook-openentry.md). Si ce paramètre est NULL ou un **MAPIUID** zéro, cette fonction agit également exactement comme [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Elle ne peut pas être NULL.
    
 _lpulUIParam_
  
> [out] Poignée vers la fenêtre parente de la boîte de dialogue.
    
 _lpfnDismiss_
  
> [in] Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** ou NULL. Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place. MAPI appelle la **fonction DISMISSMODELESS** lorsque l’utilisateur fait disparaître la boîte de dialogue d’adresses sans mode, informant un client qui appelle Details que la boîte de dialogue n’est plus active. 
    
 _lpvDismissContext_
  
> [in] Pointeur vers les informations de contexte à transmettre à la **fonction DISMISSMODELESS** pointée par le paramètre _lpfnDismiss._ Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue en incluant **l’indicateur DIALOG_SDI** dans le _paramètre ulFlags._ 
    
 _cbEntryID_
  
> [in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.
    
 _lpfButtonCallback_
  
> [in] Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON.** Une **fonction LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails. 
    
 _lpvButtonContext_
  
> [in] Pointeur vers des données qui a été utilisé comme paramètre pour la fonction spécifiée par le _paramètre lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible. Le  _paramètre lpszButtonText_ doit être NULL lorsqu’un bouton extensible n’est pas nécessaire. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte pour le _paramètre lpszButtonText._ Les indicateurs suivants peuvent être définies : 
    
AB_TELL_DETAILS_CHANGE
  
> Indique que details renvoie TRUE si des modifications sont réellement apportées à l’adresse ; Dans le cas contraire, Details renvoie FALSE.
    
DIALOG_MODAL
  
> Affiche la version modale de la boîte de dialogue d’adresse commune. Cet indicateur s’exclue mutuellement avec DIALOG_SDI.
    
DIALOG_SDI
  
> Affiche la version non modée de la boîte de dialogue d’adresse commune. Cet indicateur s’exclue mutuellement avec DIALOG_MODAL.
    
MAPI_UNICODE
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    

