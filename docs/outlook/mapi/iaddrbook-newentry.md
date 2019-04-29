---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405099"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un nouveau destinataire à un conteneur de carnet d'adresses ou à la liste des destinataires d'un message sortant.
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Handle de la fenêtre parente de la boîte de dialogue.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type du texte utilisé. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _cbEIDContainer_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> dans Pointeur vers l'identificateur d'entrée du conteneur auquel le nouveau destinataire doit être ajouté. Si le paramètre _cbEIDContainer_ est égal à zéro, la méthode **NewEntry** renvoie un identificateur d'entrée de destinataire et une liste de modèles comme si la méthode [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) était appelée. 
    
 _cbEIDNewEntryTpl_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> dans Pointeur vers un modèle isolé qui sera utilisé pour créer le nouveau destinataire. Si _cbEIDNewEntryTpl_ est égal à zéro et que _LPEIDNEWENTRYTPL_ a la valeur null, **NewEntry** affiche une boîte de dialogue dans laquelle l'utilisateur peut choisir dans une liste de modèles pour ajouter de nouvelles entrées. 
    
 _lpcbEIDNewEntry_
  
> remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée du nouveau destinataire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La création de l'entrée de carnet d'adresses a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **NewEntry** crée une nouvelle entrée de carnet d'adresses, qui doit être ajoutée directement dans un conteneur ou utilisée pour adresser un message sortant. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous souhaitez que la nouvelle entrée soit ajoutée à un conteneur spécifique, définissez _lpEIDContainer_ sur l'identificateur d'entrée du conteneur et _cbEIDContainer_ sur le nombre d'octets dans l'identificateur d'entrée. 
  
Si vous souhaitez que la nouvelle entrée soit ajoutée à la liste des destinataires d'un message sortant, affectez la valeur NULL à _lpEIDContainer_ et _cbEIDContainer_ à zéro. 
  
Si vous souhaitez permettre à l'utilisateur d'une application cliente de sélectionner le type d'entrée à créer, transmettez zéro dans _cbEIDNewEntryTpl_ et null dans _lpEIDNewEntryTpl_. La méthode **NewEntry** affiche la table ponctuelle MAPI, une liste de modèles pris en charge par MAPI et par chaque fournisseur de carnet d'adresses dans la session. Chaque modèle peut créer une entrée de destinataire pour un ou plusieurs types d'adresses. 
  
Si vous souhaitez conserver l'identificateur d'entrée de la nouvelle entrée, transmettez des pointeurs valides dans les paramètres _lpcbEIDNewEntry_ et _lppEIDNewEntry_ . Vous êtes responsable de la libération de cet identificateur d'entrée lorsque vous avez fini de l'utiliser en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour utiliser un modèle particulier afin d'ajouter une nouvelle entrée à un conteneur modifiable, procédez comme suit:
  
1. Appelez la méthode [IMAPISession:: OpenEntry](imapisession-openentry.md) pour ouvrir le conteneur de destination et définissez le paramètre _lpEntryID_ sur l'identificateur d'entrée du conteneur. 
    
2. Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur de destination et définissez le paramètre _ulPropTag_ sur **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et le paramètre _lpiid_ sur IID_IMAPITable. Le conteneur renverra une table ponctuelle qui répertorie tous les modèles pris en charge pour la création de nouvelles entrées. 
    
3. Récupérez la ligne qui représente le modèle pour le type d'entrée spécifique que vous souhaitez créer. La colonne **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indique le type d'adresse pris en charge par le modèle.
    
4. Appelez la méthode **NewEntry** et définissez _lpEIDNewEntryTpl_ sur l'identificateur d'entrée du modèle sélectionné. L'identificateur d'entrée sera la colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne du modèle dans la table One-Off. Transmettre zéro dans _cbEIDContainer_ et null dans _lpEIDContainer_. TransMettez un pointeur valide dans le paramètre _lppEIDNewEntry_ si vous souhaitez conserver l'identificateur d'entrée de la nouvelle entrée. 
    
## <a name="see-also"></a>Voir aussi



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

