---
title: Propriété canonique PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345464"
---
# <a name="pidtagsearchkey-canonical-property"></a>Propriété canonique PidTagSearchKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une clé comparable au binaire qui identifie les objets corrélés pour une recherche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x300B  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés de l’ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un suivi pour les objets associés, tels que les copies de messages, et facilite la recherche d’occurrences indésirables, telles que des destinataires en double.
  
MAPI utilise des règles spécifiques pour la construction de clés de recherche pour les destinataires du message. La clé de recherche est formée en concassant le type d’adresse (en caractères en minuscules), le caractère deux-points « : », l’adresse e-mail sous la forme canonique et le caractère null de fin. La forme canonique ici signifie que les adresses sensibles à la cas apparaissent dans le cas correct et que les adresses qui ne sont pas sensibles à la cas sont converties en minuscules. Ceci est important pour la conservation des corrélations entre les messages.
  
Pour les objets de message, cette propriété est disponible via la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) immédiatement après la création du message. Pour d’autres objets, il est disponible après le premier appel à la [méthode IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Étant donné que cette propriété est modifiable, il n’est pas fiable de l’obtenir via **GetProps** jusqu’à ce qu’un appel SaveChanges ait engagé des **valeurs définies** ou modifiées par la méthode [IMAPIProp::SetProps.](imapiprop-setprops.md) 
  
Pour les profils, MAPI fournit également une section de profil codée en dur MUID_PROFILE_INSTANCE **,** avec cette propriété comme propriété unique. Cette clé est garantie d’être unique parmi tous les profils créés et peut être plus fiable que la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), qui peut, par exemple, être supprimée et recréée avec le même nom.
  
Le tableau suivant récapitule les différences importantes entre les PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et cette propriété.
  
|**Caractéristique**|PR_ENTRYID****|PR_RECORD_KEY****|PR_SEARCH_KEY****|
|:-----|:-----|:-----|:-----|
|Obligatoire sur les objets de pièce jointe  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire pour les objets de dossier  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets de la boutique de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets d’état  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Créatable par client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Disponible avant **SaveChanges** <br/> |Dépend de l’implémentation du fournisseur  <br/> |Dépend de l’implémentation du fournisseur  <br/> |Pour les messages, Oui. Pour d’autres, cela dépend de l’implémentation du fournisseur.  <br/> |
|Modifié dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modification possible par client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique au sein de ...  <br/> |Monde entier  <br/> |Instance du fournisseur  <br/> |Monde entier  <br/> |
|Comparaison binaire (comme avec memcmp)  <br/> |No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Oui  <br/> |Oui  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Propriété canonique PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

