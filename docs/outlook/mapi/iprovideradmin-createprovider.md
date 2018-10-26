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
ms.openlocfilehash: f76b44b3718f08eb68fc956ad4480d4327cb0656
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578625"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un fournisseur de services pour le service de message. 
  
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
  
> [in] Pointeur vers le nom du fournisseur à ajouter.
    
 _cValues_
  
> [in] Le nombre de valeurs de propriété indiqué par le paramètre _lpProps_ . 
    
 _lpProps_
  
> [in] Pointeur vers un tableau de valeurs de propriété qui décrit les propriétés du fournisseur à ajouter.
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche. Le paramètre _ulUIParam_ est utilisé si l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’ajout du fournisseur. Les indicateurs suivants peuvent être définis :
    
  - MAPI_DIALOG : Affiche une boîte de dialogue pour demander des informations de configuration.
      
  - MAPI_UNICODE : Les propriétés nom et la chaîne du fournisseur sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.
    
 _lpUID_
  
> [out] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique qui représente le fournisseur à ajouter. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur a été ajouté au service de message.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IProviderAdmin::CreateProvider** ajoute un fournisseur de services pour le service de message. Le paramètre _lpszProvider_ doit pointer sur le nom d’un fournisseur qui appartient au service de message. **CreateProvider** ne vérifie pas si le nom correspond au nom d’un fournisseur de service ; Si le nom passé ne correspond pas à un nom de service, l’appel réussit, mais le résultat est imprévisible. La plupart des services de messagerie ne permettent pas de fournisseurs être ajouté ou supprimé pendant que le profil est en cours d’utilisation. 
  
Après tout des informations disponibles sur le service fournisseur a été ajouté au profil à partir du fichier Mapisvc.inf, **CreateProvider** appelle la fonction de point d’entrée du service de message avec le paramètre _ulContext_ défini sur MSG_SERVICE_ PROVIDER_CREATE. Si MAPI_DIALOG est définie dans le paramètre de la méthode **CreateProvider** _ulFlags_ , les valeurs dans les paramètres _ulUIParam_ et _ulFlags_ sont également transmises à la fonction de point d’entrée. Ces paramètres supplémentaires activer le fournisseur de services afficher sa feuille de propriétés afin que l’utilisateur puisse entrer des paramètres de configuration. 
  
## <a name="see-also"></a>Voir aussi

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

