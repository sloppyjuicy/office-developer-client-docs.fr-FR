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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: da7d19407856570a628529877252360d1537bae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595390"
---
# <a name="pidtagsearchkey-canonical-property"></a>Propriété canonique PidTagSearchKey

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une clé comparable binaire qui identifie les objets en corrélation pour une recherche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x300B  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un suivi pour les objets associés, tels que des copies de messages et facilite la recherche des occurrences indésirables, tels que les destinataires en double.
  
MAPI utilise des règles spécifiques pour construire les clés de recherche pour les destinataires du message. La clé de recherche est formée en concaténant le type d’adresse (en majuscules), le signe deux-points ' :', l’adresse de messagerie dans le formulaire canonique et le caractère de fin null. Forme canonique ici signifie que la casse adresses apparaissent dans la casse, et les adresses qui ne respectent pas la casse sont converties en majuscules. Il est important de conserver les corrélations entre les messages.
  
Pour les objets de message, cette propriété est disponible par le biais de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) immédiatement après la création du message. Pour les autres objets, il est disponible après le premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Étant donné que cette propriété est modifiable, il n’est pas fiable pour obtenir par le biais de **GetProps** jusqu'à ce qu’un appel de **SaveChanges** a validé les valeurs défini ou modifié par la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) . 
  
Pour les profils, MAPI fournit également une section de profil codé en dur nommée **MUID_PROFILE_INSTANCE**, avec cette propriété en tant que sa propriété unique. Cette clé est garantie unique parmi tous les profils jamais créés et peut être plus fiable que la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), qui peut être, par exemple, suppression et recréation portant le même nom.
  
Le tableau suivant récapitule les différences importantes entre le **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et cette propriété.
  
|**Caractéristique**|PR_ENTRYID ***|PR_RECORD_KEY ***|CLÉ PR_SEARCH_KEY ***|
|:-----|:-----|:-----|:-----|
|Requis sur les objets attachment  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets de dossier  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets de banque de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets d’état  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Qui peut être créé par client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Avant de **SaveChanges** <br/> |Dépend de l’implémentation du fournisseur  <br/> |Dépend de l’implémentation du fournisseur  <br/> |Pour les messages, Oui. Pour d’autres personnes, il dépend de l’implémentation du fournisseur.  <br/> |
|Modification dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modifiable par client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique au sein de...  <br/> |Monde entier  <br/> |Instance de fournisseur  <br/> |Monde entier  <br/> |
|Binaire comparable (comme avec memcmp)  <br/> |No : utilisez [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Oui  <br/> |Oui  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Propriété canonique PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

