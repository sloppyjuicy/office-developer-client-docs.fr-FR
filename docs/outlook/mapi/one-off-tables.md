---
title: One-Off Tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 0dfa967569a276c1a2f11248b0a166be21c4ac0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595629"
---
# <a name="one-off-tables"></a>One-Off Tables

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un tableau unique contient des informations sur les modèles qu’un fournisseur de carnet d’adresses prend en charge pour la création de destinataires. Les tables individuelles sont implémentées par des fournisseurs de carnets d’adresses, des conteneurs de carnet d’adresses individuels et par MAPI, et peuvent être persistantes ou temporaires. 
  
> [!NOTE]
> Ne confondez pas les modèles des tableaux uniques avec les identificateurs de modèle ; bien que leurs objectifs soient similaires, leurs constructions de code sont identiques. Les modèles sont utilisés pour créer des destinataires d’un type particulier, tandis que les identificateurs de modèle sont utilisés pour lier les données d’un destinataire appartenant à un fournisseur hôte avec du code pour prendre en charge un autre destinataire appartenant à un fournisseur étranger. 
  
Les clients créent de nouveaux destinataires :
  
- Pour l’ajouter à la liste des destinataires d’un message sortant.
    
- Pour l’ajouter à l’un des conteneurs du carnet d’adresses.
    
Dans les deux scénarios, un fournisseur de carnet d’adresses est invité à renvoyer une table un-off. Les fournisseurs de carnets d’adresses peuvent implémenter une seule table unique à utiliser dans les deux situations ou une table unique pour chaque situation. 
  
Lorsque le destinataire est inclus dans un message sortant, MAPI appelle la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) du fournisseur de carnet d’adresses pour récupérer sa table unie. Le tableau unique inclut des modèles qui permettent à un utilisateur d’entrer des informations qui entraînent la création d’un destinataire avec une adresse valide. MAPI s’inscrit pour les notifications sur cette table, en la conservant ouverte afin que les modifications soient reflétées pour l’utilisateur. MAPI libère la table uniquement lorsque la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) de son sous-système ou de son objet d’état de carnet d’adresses est appelée. 
  
Lorsque le destinataire est ajouté à un conteneur, MAPI effectue un appel différent, appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour récupérer sa propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). L’ensemble de modèles inclus dans ce tableau unique représente les types de destinataires qui peuvent être ajoutés au conteneur. Par exemple, les serveurs de messagerie exposent souvent un conteneur pour chaque passerelle installée afin que chaque conteneur ne conserve que des adresses spécifiques à la passerelle correspondante.
  
MAPI fournit un tableau unique qui inclut ses propres modèles, ainsi que des modèles de chacun des fournisseurs de carnet d’adresses de la session. MAPI fournit un modèle générique qui peut être utilisé pour créer un destinataire pour n’importe quel type d’adresse, en supposant que l’utilisateur connaît son format. Les fournisseurs de carnets d’adresses utilisent cette table autonome en appelant [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Chacun des modèles inclus dans le tableau unique MAPI entraîne la création de destinataires avec des adresses de destinataire valides.
  
Les fournisseurs de carnets d’adresses fournissent généralement un modèle pour chaque type d’adresse qu’ils prend en charge. Toutefois, la prise en charge des modèles n’est pas requise. Les fournisseurs de carnet d’adresses qui n’autorisent pas la création de nouvelles adresses peuvent renvoyer des MAPI_E_NO_SUPPORT lorsque MAPI appelle pour demander une table unique. Les fournisseurs de carnet d’adresses qui autorisent la création de nouvelles adresses mais qui ne fournissent aucun modèle peuvent appeler **IMAPISupport::GetOneOffTable** pour utiliser les modèles répertoriés dans le tableau unique MAPI. 
  
Les propriétés suivantes définissent le jeu de colonnes requis dans des tables uniques :
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indique le type d’adresse qui peut être associé au nouveau destinataire créé avec le modèle. 
  
 **PR_DISPLAY_NAME** et **PR_DISPLAY_TYPE** associer des données au nouveau destinataire. **PR_DISPLAY_NAME** contient une chaîne de caractères qui identifie le nouveau destinataire et **PR_DISPLAY_TYPE** contient une constante qui identifie le type d’icône à afficher avec la ligne. Les modèles pour les utilisateurs de messagerie **ont leur PR_DISPLAY_TYPE** colonne définie sur DT_MAILUSER ; Les modèles de listes de distribution ont **leur PR_DISPLAY_TYPE** colonne définie sur DT_DISTLIST. 
  
 **PR_ENTRYID** est l’identificateur d’entrée du modèle à utiliser pour créer un destinataire. Cet identificateur d’entrée peut être transmis aux futurs appels [IAddrBook::NewEntry,](iaddrbook-newentry.md) [IAddrBook::OpenEntry](iaddrbook-openentry.md)et [IABContainer::CreateEntry.](iabcontainer-createentry.md) Les conteneurs définissent la colonne **PR_ENTRYID** de leur ligne pour le modèle d’utilisateur de messagerie par défaut sur **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et la colonne **PR_ENTRYID** de leur ligne pour le modèle de liste de distribution par défaut sur **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** permet de prendre en charge l’affichage hiérarchique des entrées d’un tableau unique en indiquant le niveau de retrait du modèle. Bien qu’il soit possible d’afficher des tableaux à deux niveaux sous la direction d’une liste plate ou d’un affichage hiérarchique, il est préférable que les fournisseurs de carnets d’adresses la prise en charge en fixant la colonne **PR_DEPTH** pour chaque ligne de manière appropriée. **PR_DEPTH** est basé sur zéro ; les lignes avec la valeur 0 dans leur **colonne PR_DEPTH** ne sont pas en retrait. Plus la valeur de la **PR_DEPTH** est élevée, plus la ligne est en retrait. Par exemple, les  lignes PR_DEPTH définies sur 1 sont en retrait  d’un onglet, tandis que les lignes PR_DEPTH définies sur 3 sont en retrait de trois onglets. 
  
 **PR_SELECTABLE** permet d’indiquer si une ligne du tableau représente un modèle qui peut être sélectionné et utilisé pour créer un destinataire. Bien que la plupart des lignes d’un tableau unique représentent des modèles, les fournisseurs peuvent inclure des lignes autres que des modèles. Par exemple, un fournisseur peut organiser le tableau unique par type de modèle, y compris une ligne de catégorie qui apparaît dans l’affichage, mais qui n’est pas utilisée pour la création de destinataires. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

