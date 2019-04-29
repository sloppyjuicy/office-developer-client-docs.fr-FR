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
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411273"
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée d'un modèle pour la création de nouvelles entrées d'un type particulier. 
    
 _ulCreateFlags_
  
> dans Masque de des indicateurs qui contrôle le mode de création de l'entrée. Les indicateurs suivants peuvent être définis:
    
CREATE_CHECK_DUP_LOOSE 
  
> Un niveau faible de vérification des entrées en double doit être effectué. L'implémentation de la vérification des entrées en double libre est spécifique au fournisseur. Par exemple, un fournisseur peut définir une correspondance libre comme deux entrées portant le même nom complet.
    
CREATE_CHECK_DUP_STRICT 
  
> Un niveau strict de vérification des entrées en double doit être effectué. L'implémentation d'une vérification d'entrée stricte en double est propre au fournisseur. Par exemple, un fournisseur peut définir une correspondance stricte comme deux entrées ayant à la fois le même nom d'affichage et l'même adresse de messagerie.
    
CREATE_REPLACE 
  
> Une nouvelle entrée doit remplacer une entrée existante s'il est déterminé que les deux sont des doublons.
    
 _lppMAPIPropEntry_
  
> remarquer Pointeur vers un pointeur vers l'entrée nouvellement créée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La création de l'entrée a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IABContainer:: CreateEntry** crée une nouvelle entrée d'un type particulier dans le conteneur spécifié, en renvoyant un pointeur vers une implémentation d'interface pour un accès supplémentaire à l'entrée. La nouvelle entrée est créée à l'aide d'un modèle qui a été sélectionné dans la liste des modèles disponibles du conteneur publié dans sa table One-Off. Les appelants accèdent à la table ponctuelle d'un conteneur en appelant sa méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et en demandant la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Tous les conteneurs qui prennent en charge la méthode **IABContainer:: CreateEntry** doivent être modifiables. Définissez l'indicateur AB_MODIFIABLE de votre conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu'il est modifiable. 
  
Vous devez prendre en charge tous les indicateurs _ulCreateFlags_ . Toutefois, l'interprétation et l'utilisation de ces indicateurs sont propres à l'implémentation, autrement dit, vous pouvez déterminer les sémantiques de CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le contexte de votre implémentation. Si vous ne pouvez pas ou ne Déterminez pas si une entrée est un doublon, autorisez toujours la création de l'entrée. 
  
Certains fournisseurs implémentent une vérification stricte de l'entrée en faisant correspondre le nom complet, l'adresse de messagerie et la clé de recherche dans une entrée; les autres fournisseurs limitent la correspondance au nom complet et à l'adresse. La vérification d'entrée libre est souvent implémentée en vérifiant uniquement le nom d'affichage. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Notes pour héberger les implémenteurs de fournisseurs de carnets d'adresses

Si votre conteneur peut créer des entrées à partir des modèles d'autres fournisseurs, votre implémentation de **CreateEntry** doit fournir une partie ou la totalité des propriétés associées aux entrées créées. Par exemple, si vous fournissez un espace de stockage pour la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) d'une entrée, vous pouvez générer sa boîte de dialogue détails sans devoir compter sur le fournisseur étranger. 
  
Si votre conteneur peut créer des entrées qui prennent en charge la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), votre implémentation de **CreateEntry** doit effectuer les opérations suivantes: 
  
1. Appelez la méthode [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) . **OpenTemplateID** permet au fournisseur étranger de lier l'entrée à la nouvelle entrée en cours de création. Les fournisseurs étrangers prennent en charge ce processus de liaison pour maintenir le contrôle des entrées créées à partir de leurs modèles dans les conteneurs de fournisseurs de carnets d'adresses hôtes. 
    
2. Effectuez toute initialisation nécessaire et remplissez le nouvel objet avec toutes les propriétés de l'entrée dans le fournisseur étranger que l'objet a renvoyé dans le paramètre _lppMAPIPropNew_ à partir de **OpenTemplateID**.
    
Si **OpenTemplateID** réussit, copiez les propriétés vers l'implémentation vers laquelle pointe le paramètre _lppMAPIPropNew_ et non directement vers l'implémentation vers laquelle pointe le paramètre _lpMAPIPropData_ . Initialisez la nouvelle entrée pour une utilisation en mode hors connexion comme vous le feriez pour toute autre entrée à partir d'un fournisseur étranger. 
  
Si **OpenTemplateID** renvoie une erreur, **CreateEntry** doit échouer. Ne pas autoriser la création de l'entrée. Étant donné que le fournisseur étranger peut faire des hypothèses sur les données de votre fournisseur, ne créez pas d'entrée avec un identificateur de modèle qui n'a pas été correctement lié au fournisseur étranger. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **CreateEntry** renvoie, vous pouvez ou non accéder immédiatement à l'identificateur d'entrée de la nouvelle entrée. Certains fournisseurs de carnets d'adresses ne les rendent pas disponibles tant que vous n'avez pas appelé la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée. 
  
Bien que les indicateurs de vérification des doublons soient passés en tant que paramètres à **CreateEntry**, l'opération de vérification des doublons ne se produit qu'après l'appel de **SaveChanges** . Par conséquent, les erreurs connexes telles que MAPI_E_COLLISION, qui indique qu'une tentative de création d'une entrée déjà existante, sont renvoyées par **SaveChanges** plutôt que **CreateEntry**.
  
## <a name="see-also"></a>Voir aussi



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

