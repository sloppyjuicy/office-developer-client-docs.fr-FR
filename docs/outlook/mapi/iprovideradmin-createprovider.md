---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430804"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un fournisseur de services au service de messagerie. 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a>Paramètres

 _lpszProvider_
  
> dans Pointeur vers le nom du fournisseur à ajouter.
    
 _cValues_
  
> dans Nombre de valeurs de propriétés vers lesquelles pointe le paramètre _lpProps_ . 
    
 _lpProps_
  
> dans Pointeur vers un tableau de valeurs de propriété qui décrit les propriétés du fournisseur à ajouter.
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente de toutes les boîtes de dialogue ou fenêtres que cette méthode affiche. Le paramètre _ulUIParam_ est utilisé si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'ajout du fournisseur. Les indicateurs suivants peuvent être définis:
    
  - MAPI_DIALOG: affiche une boîte de dialogue pour demander des informations de configuration.
      
  - MAPI_UNICODE: le nom du fournisseur et les propriétés de chaîne sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, ces chaînes sont au format ANSI.
    
 _lpUID_
  
> remarquer Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique qui représente le fournisseur à ajouter. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur a été ajouté au service de messagerie.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProviderAdmin:: CreateProvider** ajoute un fournisseur de services au service de messagerie. Le paramètre _lpszProvider_ doit pointer vers le nom d'un fournisseur qui appartient au service de messagerie. **CreateProvider** ne vérifie pas si le nom correspond au nom d'un fournisseur dans le service; Si le nom transmis ne correspond pas à un nom de service, l'appel réussit, mais les résultats sont imprévisibles. La plupart des services de message n'autorisent pas l'ajout ou la suppression de fournisseurs lorsque le profil est en cours d'utilisation. 
  
Une fois que toutes les informations disponibles sur le fournisseur de services ont été ajoutées au profil à partir du fichier MAPISVC. inf, **CreateProvider** appelle la fonction de point d'entrée du service de messagerie avec le paramètre _ULCONTEXT_ défini sur MSG_SERVICE_ PROVIDER_CREATE. Si MAPI_DIALOG est défini dans le paramètre _ulFlags_ de la méthode **CreateProvider** , les valeurs des paramètres _ulUIParam_ et _ulFlags_ sont également transmises à la fonction de point d'entrée. Ces paramètres supplémentaires permettent au fournisseur de services d'afficher sa feuille de propriétés de sorte que l'utilisateur puisse entrer des paramètres de configuration. 
  
## <a name="see-also"></a>Voir aussi

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

