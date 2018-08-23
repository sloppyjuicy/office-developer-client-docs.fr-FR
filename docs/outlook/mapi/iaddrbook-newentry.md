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
ms.openlocfilehash: eaf472a380acd62cddb2c20c35335ccb1e2ce07f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585856"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ajoute un destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.
  
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
  
> [in] Handle vers la fenêtre parente de la boîte de dialogue.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte qui est utilisé. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _cbEIDContainer_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur dans lequel le nouveau destinataire doit être ajoutée. Si le paramètre _cbEIDContainer_ est égale à zéro, la méthode **NewEntry** renvoie un identificateur d’entrée du destinataire et une liste de modèles comme si la méthode [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) a été appelée. 
    
 _cbEIDNewEntryTpl_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [in] Pointeur vers un modèle unique qui sera utilisé pour créer le nouveau destinataire. Si _cbEIDNewEntryTpl_ est égale à zéro et _lpEIDNewEntryTpl_ est NULL, **NewEntry** affiche une boîte de dialogue avec laquelle l’utilisateur peut sélectionner dans une liste de modèles pour l’ajout de nouvelles entrées. 
    
 _lpcbEIDNewEntry_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du nouveau destinataire.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La nouvelle entrée de carnet d’adresses a été créée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **NewEntry** crée une nouvelle adresse entrée de l’annuaire à ajouter directement dans un conteneur ou à utiliser pour envoyer un message sortant. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si vous souhaitez que la nouvelle entrée à ajouter à un conteneur spécifique, la valeur _lpEIDContainer_ identificateur d’entrée et de _cbEIDContainer_ pour le nombre d’octets dans l’identificateur d’entrée du conteneur. 
  
Si vous souhaitez que la nouvelle entrée à ajouter à la liste des destinataires d’un message sortant, la valeur _lpEIDContainer_ NULL et _cbEIDContainer_ à zéro. 
  
Si vous souhaitez permettre à l’utilisateur d’une application cliente pour sélectionner le type d’entrée à créer, passez zéro dans _cbEIDNewEntryTpl_ et NULL dans _lpEIDNewEntryTpl_. La méthode **NewEntry** affiche la table unique MAPI, une liste de modèles pris en charge par MAPI et par chaque fournisseur de carnet d’adresses dans la session. Chaque modèle peut créer une entrée pour un ou plusieurs types d’adresse du destinataire. 
  
Si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée, passez les paramètres _lpcbEIDNewEntry_ et _lppEIDNewEntry_ pointeurs valides. Vous êtes responsable de libérer de l’identificateur d’entrée lorsque vous avez terminé de l’utiliser en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour utiliser un modèle particulier pour ajouter une nouvelle entrée à un conteneur modifiable, utilisez la procédure suivante :
  
1. Appelez la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir le conteneur de destination et définissez le paramètre _lpEntryID_ à l’identificateur d’entrée du conteneur. 
    
2. Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) méthode du conteneur destination et définissez le paramètre _ulPropTag_ **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et le paramètre _lpiid_ sur IID_IMAPITable. Le conteneur renvoie un tableau unique qui répertorie tous les modèles pris en charge pour la création de nouvelles entrées. 
    
3. Récupérer la ligne qui représente le modèle pour le type particulier d’entrée que vous souhaitez créer. La colonne **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indique le type d’adresse est pris en charge par le modèle.
    
4. Appelez la méthode **NewEntry** et définissez _lpEIDNewEntryTpl_ sur l’identificateur d’entrée du modèle sélectionné. L’identificateur d’entrée sera la colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne du modèle dans la table unique. Passez zéro dans _cbEIDContainer_ et NULL dans _lpEIDContainer_. Passez un pointeur valid dans le paramètre _lppEIDNewEntry_ si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée. 
    
## <a name="see-also"></a>Voir aussi



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

