---
title: IMAPISupportNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
ms.openlocfilehash: 293fdd1e8a1d39ba16636ac166c337384230cbef
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371939"
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
  
> [in] Poignée vers la fenêtre parente de la boîte de dialogue.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cbEIDContainer_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur pour recevoir la nouvelle entrée. Si  _cbEIDContainer_ a la valeur 0 et  _que lpEIDContainer_ a la valeur NULL, **NewEntry** crée un identificateur d’entrée unique du même type que celui généré par un appel à la méthode [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [in] Pointeur vers l’identificateur d’entrée du modèle à utiliser pour créer la nouvelle entrée. Si  _cbEIDNewEntryTpl_ a la valeur 0 et  _que lpEIDNewEntryTpl_ a la valeur NULL, **NewEntry** affiche une boîte de dialogue qui permet à l’utilisateur de choisir dans une liste de modèles pour l’ajout de nouvelles entrées. 
    
 _lpcbEIDNewEntry_
  
> [out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par  _le paramètre lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée de l’entrée nouvellement créée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La nouvelle entrée a été créée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::NewEntry** est implémentée pour les objets de prise en charge du fournisseur de carnet d’adresses. Les fournisseurs de carnet d’adresses appellent **NewEntry** pour créer une entrée de carnet d’adresses à ajouter directement dans un conteneur ou à utiliser pour traiter un message sortant. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous souhaitez que la nouvelle entrée soit ajoutée à un conteneur spécifique, définissez  _lpEIDContainer_ sur l’identificateur d’entrée du conteneur et  _cbEIDContainer_ sur le nombre d’byte dans l’identificateur d’entrée. 
  
Si vous souhaitez que la nouvelle entrée soit ajoutée à la liste des destinataires d’un message sortant, définissez  _lpEIDContainer_ sur NULL et  _cbEIDContainer_ sur 0. 
  
Si vous souhaitez autoriser l’utilisateur d’une application cliente à sélectionner le type d’entrée à créer, passez 0 dans  _cbEIDNewEntryTpl_ et NULL dans  _lpEIDNewEntryTpl_. **NewEntry affiche** la table UNIQUE MAPI, une liste de modèles mapi et chacun des fournisseurs de carnet d’adresses dans la prise en charge de session. Chaque modèle peut créer une entrée de destinataire pour un ou plusieurs types d’adresses. 
  
Si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée, passez des pointeurs valides dans les paramètres _lpcbEIDNewEntry_ et  _lppEIDNewEntry_ . Vous devez libérer cet identificateur d’entrée lorsque vous en avez terminé en appelant la [fonction MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour utiliser un modèle particulier afin d’ajouter une nouvelle entrée à un conteneur modifiable, utilisez la procédure suivante :
  
1. Appelez [la méthode IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir le conteneur de destination et définissez le paramètre  _lpEntryID_ sur l’identificateur d’entrée du conteneur. 
    
2. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur de destination et définissez le paramètre  _ulPropTag_ sur **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et le paramètre  _lpiid_ sur IID_IMAPITable. Le conteneur retourne une table unique qui répertorie tous les modèles qu’il prend en charge pour la création de nouvelles entrées. 
    
3. Récupérez la ligne qui représente le modèle pour le type particulier d’entrée que vous souhaitez créer. La **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indique le type d’adresse pris en charge par le modèle. 
    
4. Appelez **IMAPISupport::NewEntry** et définissez le paramètre  _lpEIDNewEntryTpl_ sur l’identificateur d’entrée du modèle sélectionné. L’identificateur **d’entrée est PR_ENTRYID** colonne ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la ligne du modèle dans le tableau unique. Passez 0 dans  _cbEIDContainer_ et NULL dans  _lpEIDContainer_. Passez un pointeur valide dans le paramètre _lppEIDNewEntry_ si vous souhaitez conserver l’identificateur d’entrée de la nouvelle entrée. 
    
## <a name="see-also"></a>Voir aussi



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

