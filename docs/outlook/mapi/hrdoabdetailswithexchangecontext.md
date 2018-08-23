---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d882fa1e705969ae06da46710fc7216625ca932e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566375"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Garantit que la méthode **OpenEntry** est ouvert par le fournisseur de carnet d’adresses Exchange attendu. Cette fonction fonctionne comme [IAddrBook::Details](iaddrbook-details.md), mais s’ouvre **entryID** à l’aide du carnet d’adresses Exchange identifié par le paramètre _pEmsmdbUID_ . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> La session **IMAPISession**. Il ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> Pointeur vers un **emsmdbUID** qui identifie le Service Exchange qui contient le fournisseur de carnet d’adresses Exchange qui est utilisé par la fonction pour ouvrir l’identificateur d’entrée. Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée Exchange adresse livre fournisseur, ce paramètre est ignoré et la fonction se comporte comme [IAddrBook::OpenEntry](iaddrbook-openentry.md). Si ce paramètre est NULL ou un zéro **MAPIUID**, cette fonction comporte également exactement comme [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.
    
 _lpulUIParam_
  
> [out] Handle vers la fenêtre parente de la boîte de dialogue.
    
 _lpfnDismiss_
  
> [in] Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** ou NULL. Ce membre s’applique uniquement à la version de la boîte de dialogue non modale, telle qu’indiquée par l’indicateur DIALOG_SDI en cours. MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ferme la boîte de dialogue non modale adresse informant le client qui appelle plus d’informations que la boîte de dialogue n’est plus active. 
    
 _lpvDismissContext_
  
> [in] Un pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** indiqué par le paramètre _lpfnDismiss_ . Ce paramètre s’applique uniquement à la version de la boîte de dialogue non modale en incluant l’indicateur **DIALOG_SDI** dans le paramètre _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.
    
 _lpfButtonCallback_
  
> [in] Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON** . Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails. 
    
 _lpvButtonContext_
  
> [in] Pointeur vers les données qui a été utilisés en tant que paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible. Le paramètre _lpszButtonText_ doit être NULL lorsqu’un bouton extensible n’est pas nécessaire. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ . Les indicateurs suivants peuvent être définis : 
    
AB_TELL_DETAILS_CHANGE
  
> Indique que les détails renvoie la valeur TRUE si les modifications sont réellement apportées à l’adresse ; plus d’informations dans le cas contraire, renvoie la valeur FALSE.
    
DIALOG_MODAL
  
> Affiche la version de la boîte de dialogue adresse modale. Cet indicateur est mutuellement exclusif avec DIALOG_SDI.
    
DIALOG_SDI
  
> Affiche la version de la boîte de dialogue adresse non modale. Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.
    
MAPI_UNICODE
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    

