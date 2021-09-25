---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c24adf9f25ab1d8137de76b84b2f612a45b7090e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616949"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur.
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée d’un modèle pour la création d’entrées d’un type particulier. 
    
 _ulCreateFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la création d’entrée est effectuée. Les indicateurs suivants peuvent être définies :
    
CREATE_CHECK_DUP_LOOSE 
  
> Un niveau souple de vérification des entrées en double doit être effectué. L’implémentation de la vérification des entrées libres en double est spécifique au fournisseur. Par exemple, un fournisseur peut définir une correspondance souple comme deux entrées qui ont le même nom d’affichage.
    
CREATE_CHECK_DUP_STRICT 
  
> Un niveau strict de vérification des entrées en double doit être effectué. L’implémentation d’une vérification stricte des entrées en double est propre au fournisseur. Par exemple, un fournisseur peut définir une correspondance stricte comme deux entrées qui ont à la fois le même nom d’affichage et la même adresse de messagerie.
    
CREATE_REPLACE 
  
> Une nouvelle entrée doit remplacer une entrée existante s’il est déterminé que les deux sont des doublons.
    
 _lppMAPIPropEntry_
  
> [out] Pointeur vers un pointeur vers l’entrée nouvellement créée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La nouvelle entrée a été créée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IABContainer::CreateEntry** crée une entrée d’un type particulier dans le conteneur spécifié, renvoyant un pointeur vers une implémentation d’interface pour un accès supplémentaire à l’entrée. La nouvelle entrée est créée à l’aide d’un modèle qui a été sélectionné dans la liste des modèles disponibles du conteneur publiée dans son tableau unique. Les appelants accèdent à la table one-off d’un conteneur en appelant sa méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et en demandant la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Tous les conteneurs qui la prise en charge de la **méthode IABContainer::CreateEntry** doivent être modifiables. Définissez l’indicateur AB_MODIFIABLE conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu’il est modifiable. 
  
Vous devez prendre en charge tous les _indicateurs ulCreateFlags._ Toutefois, l’interprétation et l’utilisation de ces indicateurs sont spécifiques à l’implémentation, c’est-à-dire que vous pouvez déterminer ce que signifient les sémantiques de CREATE_CHECK_DUP_LOOSE et de CREATE_CHECK_DUP_STRICT dans le contexte de votre implémentation. Si vous ne pouvez pas ou ne déterminez pas si une entrée est en double, autorisez toujours la création de l’entrée. 
  
Certains fournisseurs implémentent une vérification stricte des entrées en mettant en correspondance le nom d’affichage, l’adresse de messagerie et la clé de recherche dans une entrée . d’autres fournisseurs limitent la correspondance au nom complet et à l’adresse. La vérification des entrées libres est souvent implémentée en vérifiant uniquement le nom complet. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Remarques à l’adresse des implémenteurs du fournisseur de carnet d’adresses hôte

Si votre conteneur peut créer des entrées à partir des modèles d’autres fournisseurs, votre implémentation de **CreateEntry** doit fournir un stockage pour une partie ou l’ensemble des propriétés associées aux entrées créées. Par exemple, si vous fournissez un stockage pour la propriété **PR_DETAILS_TABLE (** [PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) d’une entrée, vous pouvez générer sa boîte de dialogue de détails sans dépendre du fournisseur étranger. 
  
Si votre conteneur peut créer des entrées qui PR_TEMPLATEID **la** propriété ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), votre implémentation de **CreateEntry** doit : 
  
1. Appelez [la méthode IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md) **OpenTemplateID** permet au code du fournisseur étranger de lier l’entrée à la nouvelle entrée en cours de création. Les fournisseurs étrangers assurent la prise en charge de ce processus de liaison pour maintenir le contrôle sur les entrées créées à partir de leurs modèles dans les conteneurs des fournisseurs de carnets d’adresses hôtes. 
    
2. Effectuez toute initialisation nécessaire et remplir le nouvel objet avec toutes les propriétés de l’entrée dans le fournisseur étranger que l’objet renvoyé dans le paramètre  _lppMAPIPropNew_ à partir **d’OpenTemplateID**.
    
Si **OpenTemplateID** réussit, copiez les propriétés vers l’implémentation pointée par le paramètre _lppMAPIPropNew_ plutôt que directement vers l’implémentation pointée par le paramètre _lpMAPIPropData._ Initialisez la nouvelle entrée pour une utilisation hors connexion comme vous le feriez pour toute autre entrée provenant d’un fournisseur étranger. 
  
Si **OpenTemplateID renvoie** une erreur, **CreateEntry** doit échouer. N’autorisez pas la création de l’entrée. Étant donné que le fournisseur étranger peut effectuer des hypothèses sur les données de votre fournisseur, ne créez pas d’entrée avec un identificateur de modèle qui n’a pas été lié au fournisseur étranger. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **CreateEntry est** de retour, vous pouvez ou non accéder immédiatement à l’identificateur d’entrée de la nouvelle entrée. Certains fournisseurs de carnet d’adresses ne le rendent disponible qu’après avoir appelé la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée. 
  
Bien que les indicateurs de vérification dupliqués soient passés en tant que paramètres à **CreateEntry,** l’opération de vérification des doublons ne se produit pas tant que **SaveChanges n’est** pas appelé. Par conséquent, les erreurs associées telles que MAPI_E_COLLISION, qui indique qu’une tentative de création d’une entrée existante a été tentée, sont renvoyées par **SaveChanges** plutôt que **CreateEntry**.
  
## <a name="see-also"></a>Voir aussi



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

