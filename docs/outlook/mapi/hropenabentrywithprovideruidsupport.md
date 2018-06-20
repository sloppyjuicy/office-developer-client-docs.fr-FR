---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bd42fcd34042c2f9579497f164c4a67f6ba97e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783584"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**S’applique à**: Outlook 
  
Effectue la même fonction que la fonction [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) , sauf que la fonction **HrOpenABEntryWithProviderUIDSupport** ouvre l’entrée à l’aide de l’objet de prise en charge donné au lieu d’utiliser la session et le carnet d’adresses. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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

## <a name="parameters"></a>Paramètres

 _pEmsabpUID_
  
> [in] Pointeur vers un paramètre _emsabpUID_ qui identifie le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher plus d’informations sur l’identificateur d’entrée. Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée Exchange adresse livre fournisseur, ce paramètre est ignoré et la fonction appel exactement joue [IAddrBook::Details](iaddrbook-details.md). Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction comporte également exactement comme [IAddrBook::Details](iaddrbook-details.md).
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée open. Passage de NULL renvoie l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md)et il s’agit de conteneurs [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage. 
    
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
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’entrée ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur de l’entrée ouvert.
    

