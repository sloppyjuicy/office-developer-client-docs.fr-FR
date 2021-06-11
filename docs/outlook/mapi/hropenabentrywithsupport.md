---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417643"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
N’utilisez pas cette fonction.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.
    
 _lpInterface_
  
>  [in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée ouverte. La transmission NULL renvoie l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard [est IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s’agit de [IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s’agit de [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir  _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage. 
    
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
    

