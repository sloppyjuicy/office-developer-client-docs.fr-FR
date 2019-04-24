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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3468e4a92787e440f230d60ab31f37526fe7d5e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316641"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un nouveau destinataire directement à un conteneur de carnet d'adresses ou à la liste des destinataires d'un message sortant.
  
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
  
> dans Handle de la fenêtre parent de la boîte de dialogue.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cbEIDContainer_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> dans Pointeur vers l'identificateur d'entrée du conteneur auquel la nouvelle entrée doit être reçue. Si _cbEIDContainer_ est égal à 0 et que _LPEIDCONTAINER_ a la valeur null, **NewEntry** crée un identificateur d'entrée unique qui est le même type que celui généré par un appel à la méthode [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> dans Pointeur vers l'identificateur d'entrée du modèle à utiliser pour créer la nouvelle entrée. Si _cbEIDNewEntryTpl_ a la valeur 0 et que _LPEIDNEWENTRYTPL_ a la valeur null, **NewEntry** affiche une boîte de dialogue qui permet à l'utilisateur d'effectuer une sélection dans une liste de modèles pour l'ajout de nouvelles entrées. 
    
 _lpcbEIDNewEntry_
  
> remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée de l'entrée nouvellement créée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La création de l'entrée a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: NewEntry** est implémentée pour les objets de prise en charge du fournisseur de carnets d'adresses. Les fournisseurs de carnets d'adresses appellent **NewEntry** pour créer une nouvelle entrée de carnet d'adresses à ajouter directement dans un conteneur ou pour servir à adresser un message sortant. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous souhaitez que la nouvelle entrée soit ajoutée à un conteneur spécifique, définissez _lpEIDContainer_ sur l'identificateur d'entrée du conteneur et _cbEIDContainer_ sur le nombre d'octets dans l'identificateur d'entrée. 
  
Si vous souhaitez que la nouvelle entrée soit ajoutée à la liste des destinataires d'un message sortant, définissez _lpEIDContainer_ sur null et _cbEIDContainer_ sur 0. 
  
Si vous souhaitez permettre à l'utilisateur d'une application cliente de sélectionner le type d'entrée à créer, transmettez 0 dans _cbEIDNewEntryTpl_ et null dans _lpEIDNewEntryTpl_. **NewEntry** affiche la table ponctuelle MAPI, une liste de modèles que MAPI et chacun des fournisseurs de carnet d'adresses de la session prennent en charge. Chaque modèle peut créer une entrée de destinataire pour un ou plusieurs types d'adresses. 
  
Si vous souhaitez conserver l'identificateur d'entrée de la nouvelle entrée, transmettez des pointeurs valides dans les paramètres _lpcbEIDNewEntry_ et _lppEIDNewEntry_ . Vous êtes responsable de la libération de cet identificateur d'entrée lorsque vous avez fini de l'utiliser en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour utiliser un modèle particulier afin d'ajouter une nouvelle entrée à un conteneur modifiable, procédez comme suit:
  
1. Appelez la méthode [IMAPISupport:: OpenEntry](imapisupport-openentry.md) pour ouvrir le conteneur de destination et définissez le paramètre _lpEntryID_ sur l'identificateur d'entrée du conteneur. 
    
2. Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur de destination et définissez le paramètre _ulPropTag_ sur **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et le paramètre _lpiid_ sur IID_IMAPITable. Le conteneur renverra une table ponctuelle qui répertorie tous les modèles pris en charge pour la création de nouvelles entrées. 
    
3. Récupérez la ligne qui représente le modèle pour le type d'entrée spécifique que vous souhaitez créer. La colonne **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indique le type d'adresse pris en charge par le modèle. 
    
4. Appelez **IMAPISupport:: NewEntry** et définissez le paramètre _lpEIDNewEntryTpl_ sur l'identificateur d'entrée du modèle sélectionné. L'identificateur d'entrée est la colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la ligne du modèle dans la table One-Off. Transmettre 0 dans _cbEIDContainer_ et null dans _lpEIDContainer_. TransMettez un pointeur valide dans le paramètre _lppEIDNewEntry_ si vous souhaitez conserver l'identificateur d'entrée de la nouvelle entrée. 
    
## <a name="see-also"></a>Voir aussi



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

