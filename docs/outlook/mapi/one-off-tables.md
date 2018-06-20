---
title: Tables uniques
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Dernière modification : 08 novembre 2011'
ms.openlocfilehash: 3ad9141f2530e64664a2d0c75ece2b834cc6ad78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784913"
---
# <a name="one-off-tables"></a>Tables uniques

**S’applique à**: Outlook 
  
Une table unique contient des informations sur les modèles qui prend en charge par un fournisseur de carnet d’adresses pour la création de nouveaux destinataires. Tables uniques sont implémentés par les fournisseurs de carnet d’adresses, conteneurs de carnet d’adresses individuel et MAPI et peuvent être persistante ou temporaire. 
  
> [!NOTE]
> Ne confondez pas les modèles dans des tables uniques avec des identificateurs de modèle ; alors que leurs fonctions sont identiques, leurs constructions de code sont similaires nothing. Modèles utilisés pour créer les destinataires d’un type particulier pendant les identificateurs de modèle sont utilisées pour lier les données d’un destinataire qui appartiennent à un fournisseur de l’hôte avec le code pour prendre en charge un autre destinataire qui appartiennent à un fournisseur étranger. 
  
Clients créer de nouveaux destinataires :
  
- Pour ajouter à la liste des destinataires d’un message sortant.
    
- Ajouter à un des conteneurs dans le carnet d’adresses.
    
Dans les deux scénarios, un fournisseur de carnet d’adresses est demandé de renvoyer une table unique. Fournisseurs de carnet d’adresses peuvent implémenter une seule table unique à être utilisé dans les situations ou une table unique unique pour chaque situation. 
  
Lorsque le destinataire sera inclus dans un message sortant, MAPI appelle la méthode de [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) du fournisseur de carnet d’adresses pour récupérer sa table unique. Le tableau unique inclut des modèles qui permettent à un utilisateur d’entrer les informations résultant de la création d’un destinataire avec une adresse valide. Registres MAPI pour les notifications sur cette table, en conservant l’ouvrent afin que les modifications peuvent être reflétées à l’utilisateur. MAPI libère le tableau uniquement lorsque son sous-système ou l’adresse livre état [IMAPIStatus::ValidateState](imapistatus-validatestate.md) méthode de l’objet est appelée. 
  
Lorsque le destinataire sera ajouté à un conteneur, MAPI effectue un appel différents, appel de méthode [d’IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour récupérer sa propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). L’ensemble des modèles inclus dans ce tableau unique représente les types de destinataires qui peuvent être ajoutés au conteneur. Par exemple, les serveurs de messagerie exposent souvent un conteneur pour chaque passerelle est installée de sorte que chaque conteneur conserve uniquement des adresses spécifiques à la passerelle correspondante.
  
MAPI fournit un tableau unique qui inclut ses propres modèles, ainsi que les modèles de chaque les fournisseurs de carnet d’adresses dans la session. MAPI fournit un modèle générique qui peut être utilisé pour créer un destinataire pour n’importe quel type d’adresse, en partant du principe que l’utilisateur connaît son format. Fournisseurs de carnet d’adresses utilisent ce tableau unique en appelant [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Chacun des modèles inclus dans les résultats de la table uniques MAPI dans la création de destinataires dont l’adresse de destinataire valide.
  
Fournisseurs de carnet d’adresses fournissent généralement un modèle pour chaque type d’adresse qu’ils prennent en charge. Toutefois, la prise en charge de modèles n’est pas obligatoire. Fournisseurs de carnet d’adresses qui n’autorisent pas la création de nouvelles adresses peuvent renvoyer MAPI_E_NO_SUPPORT lorsque les appels MAPI pour demander une table unique. Fournisseurs de carnet d’adresses qui n’autorisent pas la création de nouvelle adresse mais ne fournissent pas de tous les modèles peuvent appeler **IMAPISupport::GetOneOffTable** pour utiliser les modèles répertoriés dans le tableau unique MAPI. 
  
Les propriétés suivantes constituent la colonne requise définie dans les tableaux uniques :
  
- **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **TYPEADR_PR** indique le type d’adresse peut être associé avec le nouveau destinataire créé avec le modèle. 
  
 **PR_DISPLAY_NAME** et **PR_DISPLAY_TYPE** associent des données avec le nouveau destinataire. **PR_DISPLAY_NAME** contient une chaîne de caractères qui identifie le nouveau destinataire et **PR_DISPLAY_TYPE** contient une constante qui identifie le type d’icône à afficher avec la ligne. Modèles pour les utilisateurs de messagerie ont leur colonne **PR_DISPLAY_TYPE** DT_MAILUSER ; modèles de listes de distribution ont leur colonne **PR_DISPLAY_TYPE** DT_DISTLIST. 
  
 **PR_ENTRYID** est l’identificateur d’entrée du modèle à utiliser pour créer un nouveau destinataire. Cet identificateur d’entrée peut être transmis à des appels futurs [IAddrBook::NewEntry](iaddrbook-newentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md)et [IABContainer::CreateEntry](iabcontainer-createentry.md) . Conteneurs de définir la colonne **PR_ENTRYID** de leur ligne pour le modèle utilisateur pour **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et la colonne **PR_ENTRYID** de leur ligne pour la liste de distribution par défaut de la messagerie par défaut modèle de **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** est utilisé pour prendre en charge l’affichage hiérarchique des entrées dans un tableau unique en indiquant le niveau de retrait pour le modèle. Bien que les tables uniques peuvent être affichées sous la forme d’une liste ou un affichage hiérarchique, cette dernière est préférable et fournisseurs de carnet d’adresses doivent prendre en charge qu’il en définissant la colonne **PR_DEPTH** pour chaque ligne de manière appropriée. **PR_DEPTH** est zéro ; lignes avec une valeur de 0 dans la colonne **PR_DEPTH** ne sont pas mis en retrait. Plus la valeur de **PR_DEPTH**est élevée, plus la ligne est mis en retrait. Par exemple, lignes avec **PR_DEPTH** défini sur 1 sont mis en retrait d’un onglet tandis que les lignes avec la valeur **PR_DEPTH** 3 sont mis en retrait de trois onglets. 
  
 **PR_SELECTABLE** sert à indiquer si une ligne de la table représente un modèle qui peut être sélectionné et permet de créer un nouveau destinataire. Bien que la plupart des lignes d’un tableau unique représentent des modèles, fournisseurs peuvent inclure des lignes non liée au modèle. Par exemple, un fournisseur souhaiterez organiser la table unique par type de modèle, y compris une ligne de catégorie qui apparaît dans l’affichage, mais n’est pas utilisée pour la création du destinataire. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

