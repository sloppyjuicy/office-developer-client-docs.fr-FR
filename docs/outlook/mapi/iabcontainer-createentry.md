---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2f8a6baa9a910b91e633084f1d9cd8ac52b24d5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575601"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une nouvelle entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur.
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Le nombre d’octets de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée d’un modèle pour la création de nouvelles entrées d’un type particulier. 
    
 _ulCreateFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la création d’entrée est effectuée. Les indicateurs suivants peuvent être définis :
    
CREATE_CHECK_DUP_LOOSE 
  
> Un niveau de vérification de l’entrée en double libre doit être effectué. L’implémentation de vérification de l’entrée en double en vrac est spécifique au fournisseur. Par exemple, un fournisseur peut définir une correspondance partielle, comme les deux entrées qui ont le même nom d’affichage.
    
CREATE_CHECK_DUP_STRICT 
  
> Un niveau strict de vérification de l’entrée en double doit être effectué. L’implémentation de vérification stricte entrée en double est spécifique au fournisseur. Par exemple, un fournisseur peut définir une correspondance exacte comme les deux entrées qui ont à la fois le même nom et l’adresse de messagerie.
    
CREATE_REPLACE 
  
> Une nouvelle entrée doit remplacer un s’il est déterminé que les deux sont des doublons.
    
 _lppMAPIPropEntry_
  
> [out] Pointeur vers un pointeur vers l’entrée nouvellement créée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La nouvelle entrée a été créée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IABContainer::CreateEntry** crée une nouvelle entrée d’un type particulier dans le conteneur spécifié, qui retourne un pointeur vers une implémentation de l’interface pour l’accès à l’entrée. La nouvelle entrée est créée à l’aide d’un modèle qui a été sélectionné à partir de la liste du conteneur des modèles disponibles publié dans sa table unique. Les appelants accéder table uniques d’un conteneur en appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et demande la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Tous les conteneurs qui prennent en charge la méthode **IABContainer::CreateEntry** doivent être modifiables. Définir l’indicateur AB_MODIFIABLE de votre conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu’il est modifiable. 
  
Vous devez prendre en charge tous les indicateurs _ulCreateFlags_ . Toutefois, l’interprétation et l’utilisation de ces indicateurs est spécifique à l’implémentation — autrement dit, vous pouvez déterminer la signification de la sémantique de CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le cadre de votre implémentation. Si vous ne pouvez pas ou ne déterminez pas si une entrée est un doublon, toujours autoriser l’entrée doit être créé. 
  
Certains fournisseurs implémentent stricte entrée vérification en comparant le nom complet, la messagerie adresse et la clé de recherche dans une entrée ; autres fournisseurs limitent la correspondance pour afficher le nom et l’adresse. Vérification de l’entrée en vrac est souvent implémenté en vérifiant seulement le nom d’affichage. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Remarques pour héberger l’adresse de l’implémentation de fournisseur livre

Si votre conteneur peut créer des entrées à partir des modèles d’autres fournisseurs, votre implémentation de **CreateEntry** doit offrir de stockage pour certaines ou toutes les propriétés associées les écritures créées. Par exemple, si vous fournissez un stockage pour une propriété du **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)), vous pouvez générer la boîte de dialogue Détails sans devoir dépendent du fournisseur étranger. 
  
Si votre conteneur peut créer des entrées qui prennent en charge la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), votre implémentation de **CreateEntry** procédez comme suit : 
  
1. Appelez la méthode [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) . **OpenTemplateID** permet de code du fournisseur étranger pour l’entrée à lier à la nouvelle entrée en cours de création. Fournisseurs étrangers prennent en charge ce processus de liaison pour contrôler les entrées créées à partir de leurs modèles dans les conteneurs de fournisseurs de carnet d’adresses hôte. 
    
2. Effectuer toute initialisation nécessaire et remplir le nouvel objet avec toutes les propriétés de l’entrée dans le fournisseur de l’objet retourné dans le paramètre _lppMAPIPropNew_ **d’OpenTemplateID**étrangère.
    
Si **OpenTemplateID** réussit, copiez les propriétés à l’implémentation désignés par le paramètre _lppMAPIPropNew_ plutôt que directement à l’implémentation désignés par le paramètre _lpMAPIPropData_ . Initialiser la nouvelle entrée pour une utilisation en mode hors connexion, comme vous le feriez pour n’importe quel autre entrée d’un fournisseur externe. 
  
Si **OpenTemplateID** renvoie une erreur, **CreateEntry** doit échouer. Ne pas autoriser l’entrée doit être créé. Étant donné que le fournisseur étranger peut émettre des hypothèses sur les données dans votre fournisseur, ne pas créer une entrée avec un identificateur de modèle qui n’a pas été correctement lié au fournisseur étranger. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsque **CreateEntry** renvoie, vous pouvez ou ne sont peut-être pas en mesure d’accéder immédiatement à l’identificateur d’entrée pour la nouvelle entrée. Certains fournisseurs de carnet d’adresses n’apportez il disponibles qu’une fois que vous avez appelé la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée. 
  
Bien que les indicateurs de vérification en double sont transmis en tant que paramètres à **CreateEntry**, le doublon opération de vérification ne se produit pas jusqu'à ce que **SaveChanges** est appelée. Par conséquent, les erreurs associées, telles que MAPI_E_COLLISION, ce qui indique qu’une tentative a été effectuée pour créer une entrée existante, sont renvoyées par **SaveChanges** plutôt que **CreateEntry**.
  
## <a name="see-also"></a>Voir aussi



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

