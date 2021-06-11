---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409544"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue la même fonction que la fonction [HrOpenABEntryWithProviderUID,](hropenabentrywithprovideruid.md) sauf que la fonction **HrOpenABEntryWithProviderUIDSupport** ouvre l’entrée à l’aide de l’objet de support donné au lieu d’utiliser la session et le carnet d’adresses. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _pEmsabpUID_
  
> [in] Pointeur vers un _paramètre emsabpUID_ qui identifie le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée. Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée de fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction agit exactement comme [IAddrBook::D etails](iaddrbook-details.md). Si ce paramètre est NULL ou un MAPIUID zéro, cette fonction agit également exactement comme [IAddrBook::D etails](iaddrbook-details.md).
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée ouverte. La transmission NULL renvoie l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard [est IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s’agit [d’IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs il s’agit de [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir  _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage. 
    
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
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’entrée ouverte.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur de l’entrée ouverte.
    

