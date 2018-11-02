---
title: IMAPISupportNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d978b7a6bd8af9a505fa025aef2e5da68308468f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588593"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un nouveau destinataire directement à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.
  
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
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cbEIDContainer_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur pour recevoir la nouvelle entrée. Si _cbEIDContainer_ est 0 et _lpEIDContainer_ a la valeur NULL, **NewEntry** crée un identificateur d’entrée unique qui est du même type que celui généré par un appel à la méthode [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [in] Pointeur vers l’identificateur d’entrée du modèle à utiliser pour créer la nouvelle entrée. Si _cbEIDNewEntryTpl_ est 0 et _lpEIDNewEntryTpl_ a la valeur NULL, **NewEntry** affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner dans une liste de modèles pour l’ajout de nouvelles entrées. 
    
 _lpcbEIDNewEntry_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée de l’entrée nouvellement créée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La nouvelle entrée a été créée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::NewEntry** est implémentée pour les objets de prise en charge du fournisseur adresse téléchargeable. Fournisseurs de carnet d’adresses appellent **NewEntry** pour créer une entrée de carnet d’adresse à ajouter directement dans un conteneur ou à utiliser pour envoyer un message sortant. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si vous souhaitez que la nouvelle entrée à ajouter à un conteneur spécifique, la valeur _lpEIDContainer_ identificateur d’entrée et de _cbEIDContainer_ pour le nombre d’octets dans l’identificateur d’entrée du conteneur. 
  
Si vous souhaitez que la nouvelle entrée à ajouter à la liste des destinataires d’un message sortant, la valeur _lpEIDContainer_ NULL et _cbEIDContainer_ sur 0. 
  
Si vous souhaitez permettre à l’utilisateur d’une application cliente pour sélectionner le type d’entrée à créer, passez 0 dans _cbEIDNewEntryTpl_ et NULL dans _lpEIDNewEntryTpl_. **NewEntry** affiche la table unique MAPI, une liste de modèles qui prennent en charge MAPI et pour tous les fournisseurs de carnet d’adresses dans la session. Chaque modèle peut créer une entrée pour un ou plusieurs types d’adresse du destinataire. 
  
Si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée, passez les paramètres _lpcbEIDNewEntry_ et _lppEIDNewEntry_ pointeurs valides. Vous êtes responsable de libérer de l’identificateur d’entrée lorsque vous avez terminé de l’utiliser en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour utiliser un modèle particulier pour ajouter une nouvelle entrée à un conteneur modifiable, utilisez la procédure suivante :
  
1. Appelez la méthode [IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir le conteneur de destination et définissez le paramètre _lpEntryID_ à l’identificateur d’entrée du conteneur. 
    
2. Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) méthode du conteneur destination et définissez le paramètre _ulPropTag_ **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et le paramètre _lpiid_ sur IID_IMAPITable. Le conteneur renvoie un tableau unique qui répertorie tous les modèles pris en charge pour la création de nouvelles entrées. 
    
3. Récupérer la ligne qui représente le modèle pour le type particulier d’entrée que vous souhaitez créer. La colonne **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indique le type d’adresse est pris en charge par le modèle. 
    
4. Appelez **IMAPISupport::NewEntry** et définissez le paramètre _lpEIDNewEntryTpl_ à l’identificateur d’entrée du modèle sélectionné. L’identificateur d’entrée est la colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne du modèle dans la table unique. Passez 0 dans _cbEIDContainer_ et NULL dans _lpEIDContainer_. Passez un pointeur valid dans le paramètre _lppEIDNewEntry_ si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée. 
    
## <a name="see-also"></a>Voir aussi



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

