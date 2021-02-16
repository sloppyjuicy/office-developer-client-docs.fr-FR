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
  
Ajoute un nouveau destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.
  
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
  
> [in] Poignée vers la fenêtre parente de la boîte de dialogue.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte utilisé. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _cbEIDContainer_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEIDContainer._ 
    
 _lpEIDContainer_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur où le nouveau destinataire doit être ajouté. Si le paramètre  _cbEIDContainer_ est zéro, la méthode **NewEntry** renvoie un identificateur d’entrée de destinataire et une liste de modèles comme si la méthode [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) était appelée. 
    
 _cbEIDNewEntryTpl_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEIDNewEntryTpl._ 
    
 _lpEIDNewEntryTpl_
  
> [in] Pointeur vers un modèle unique qui sera utilisé pour créer le nouveau destinataire. Si  _cbEIDNewEntryTpl_ est zéro et  _lpEIDNewEntryTpl_ est NULL, **NewEntry** affiche une boîte de dialogue avec laquelle l’utilisateur peut choisir dans une liste de modèles pour l’ajout de nouvelles entrées. 
    
 _lpcbEIDNewEntry_
  
> [out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par _le paramètre lppEIDNewEntry._ 
    
 _lppEIDNewEntry_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du nouveau destinataire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La nouvelle entrée de carnet d’adresses a été créée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode NewEntry** crée une entrée de carnet d’adresses, à ajouter directement dans un conteneur ou à utiliser pour traiter un message sortant. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous souhaitez que la nouvelle entrée soit ajoutée à un conteneur spécifique, définissez  _lpEIDContainer_ sur l’identificateur d’entrée du conteneur et  _cbEIDContainer_ sur le nombre d’byte dans l’identificateur d’entrée. 
  
Si vous souhaitez que la nouvelle entrée soit ajoutée à la liste des destinataires d’un message sortant, définissez  _lpEIDContainer_ sur NULL et  _cbEIDContainer_ sur zéro. 
  
Si vous souhaitez autoriser l’utilisateur d’une application cliente à sélectionner le type d’entrée à créer, passez zéro dans  _cbEIDNewEntryTpl_ et NULL dans  _lpEIDNewEntryTpl_. La **méthode NewEntry** affiche la table UNIQUE MAPI, une liste de modèles pris en charge par MAPI et par chaque fournisseur de carnet d’adresses dans la session. Chaque modèle peut créer une entrée de destinataire pour un ou plusieurs types d’adresses. 
  
Si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée, passez des pointeurs valides dans les paramètres _lpcbEIDNewEntry_ et _lppEIDNewEntry._ Vous devez libérer cet identificateur d’entrée lorsque vous en avez terminé en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md) 
  
Pour utiliser un modèle particulier afin d’ajouter une nouvelle entrée à un conteneur modifiable, utilisez la procédure suivante :
  
1. Appelez [la méthode IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir le conteneur de destination et définissez le paramètre  _lpEntryID_ sur l’identificateur d’entrée du conteneur. 
    
2. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur de destination et définissez le paramètre  _ulPropTag_ sur **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et le paramètre  _lpiid_ sur IID_IMAPITable. Le conteneur retourne une table unique qui répertorie tous les modèles qu’il prend en charge pour la création de nouvelles entrées. 
    
3. Récupérez la ligne qui représente le modèle pour le type particulier d’entrée que vous souhaitez créer. La **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indique le type d’adresse pris en charge par le modèle.
    
4. Appelez **la méthode NewEntry** et définissez  _lpEIDNewEntryTpl_ sur l’identificateur d’entrée du modèle sélectionné. L’identificateur **d’entrée sera PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne du modèle dans le tableau unique. Passez zéro dans  _cbEIDContainer_ et NULL dans  _lpEIDContainer_. Passez un pointeur valide dans le paramètre  _lppEIDNewEntry_ si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée. 
    
## <a name="see-also"></a>Voir aussi



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

