---
title: tables One-Off
description: Une table unique contient des informations sur les modèles pris en charge par un fournisseur de carnets d’adresses pour la création de nouveaux destinataires.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
ms.openlocfilehash: 931323780af036b410834e7e90fdcf92c477b868
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852683"
---
# <a name="one-off-tables"></a>tables One-Off

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table unique contient des informations sur les modèles pris en charge par un fournisseur de carnets d’adresses pour la création de nouveaux destinataires. Les tables uniques sont implémentées par des fournisseurs de carnets d’adresses, des conteneurs de carnets d’adresses individuels et par MAPI, et peuvent être persistantes ou temporaires. 
  
> [!NOTE]
> Ne confondez pas les modèles des tables uniques avec les identificateurs de modèle ; bien que leurs objectifs soient similaires, leurs constructions de code ne se ressemblent pas. Les modèles sont utilisés pour créer des destinataires d’un type particulier, tandis que les identificateurs de modèle sont utilisés pour lier les données d’un destinataire appartenant à un fournisseur hôte avec du code pour prendre en charge un autre destinataire appartenant à un fournisseur étranger. 
  
Les clients créent de nouveaux destinataires :
  
- Pour ajouter à la liste des destinataires d’un message sortant.
    
- Pour ajouter à l’un des conteneurs du carnet d’adresses.
    
Dans les deux scénarios, un fournisseur de carnet d’adresses est invité à retourner une table unique. Les fournisseurs de carnets d’adresses peuvent implémenter une table unique à utiliser dans les deux situations ou une table unique unique pour chaque situation. 
  
Lorsque le destinataire est inclus dans un message sortant, MAPI appelle la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) du fournisseur de carnet d’adresses pour récupérer sa table unique. La table unique inclut des modèles qui permettent à un utilisateur d’entrer des informations qui entraînent la création d’un destinataire avec une adresse valide. MAPI s’inscrit pour les notifications sur cette table, en la gardant ouverte afin que les modifications puissent être répercutées sur l’utilisateur. MAPI libère la table uniquement lorsque la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) de son sous-système ou de son carnet d’adresses est appelée. 
  
Lorsque le destinataire est ajouté à un conteneur, MAPI effectue un autre appel, en appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour récupérer sa propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). L’ensemble de modèles inclus dans cette table unique représente les types de destinataires qui peuvent être ajoutés au conteneur. Par exemple, les serveurs de messagerie exposent souvent un conteneur pour chaque passerelle installée afin que chaque conteneur ne conserve que des adresses spécifiques à la passerelle correspondante.
  
MAPI fournit une table unique qui inclut ses propres modèles ainsi que des modèles de chacun des fournisseurs de carnets d’adresses de la session. MAPI fournit un modèle générique qui peut être utilisé pour créer un destinataire pour n’importe quel type d’adresse, en supposant que l’utilisateur connaît son format. Les fournisseurs de carnets d’adresses utilisent cette table unique en appelant [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Chacun des modèles inclus dans la table unique MAPI entraîne la création de destinataires avec des adresses de destinataire valides.
  
Les fournisseurs de carnets d’adresses fournissent généralement un modèle pour chaque type d’adresse qu’ils prennent en charge. Toutefois, la prise en charge des modèles n’est pas nécessaire. Les fournisseurs de carnets d’adresses qui n’autorisent pas la création de nouvelles adresses peuvent retourner MAPI_E_NO_SUPPORT lorsque MAPI appelle pour demander une table unique. Les fournisseurs de carnets d’adresses qui autorisent la création de nouvelles adresses, mais qui ne fournissent aucun modèle, peuvent appeler **IMAPISupport::GetOneOffTable** pour utiliser les modèles répertoriés dans la table unique MAPI. 
  
Les propriétés suivantes constituent la colonne requise définie dans les tables uniques :
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indique le type d’adresse qui peut être associé au nouveau destinataire créé avec le modèle. 
  
 **PR_DISPLAY_NAME** et **PR_DISPLAY_TYPE** associer des données au nouveau destinataire. **PR_DISPLAY_NAME** contient une chaîne de caractères qui identifie le nouveau destinataire et **PR_DISPLAY_TYPE** contient une constante qui identifie le type d’icône à afficher avec la ligne. Les modèles pour les utilisateurs de messagerie ont leur colonne **PR_DISPLAY_TYPE** définie sur DT_MAILUSER ; Les modèles de listes de distribution ont leur colonne **PR_DISPLAY_TYPE** définie sur DT_DISTLIST. 
  
 **PR_ENTRYID** est l’identificateur d’entrée du modèle à utiliser pour créer un destinataire. Cet identificateur d’entrée peut être passé aux futurs appels [IAddrBook::NewEntry](iaddrbook-newentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md) et [IABContainer::CreateEntry](iabcontainer-createentry.md) . Les conteneurs définissent la colonne **PR_ENTRYID** de leur ligne pour le modèle d’utilisateur de messagerie par défaut **sur PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et la colonne **PR_ENTRYID** de leur ligne pour le modèle de liste de distribution par défaut **sur PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** est utilisé pour prendre en charge l’affichage hiérarchique des entrées dans une table unique en indiquant le niveau de mise en retrait du modèle. Bien que les tables uniques puissent être affichées sous la forme d’une liste plate ou d’un affichage hiérarchique, celle-ci est préférable et les fournisseurs de carnets d’adresses doivent la prendre en charge en définissant la colonne **PR_DEPTH** pour chaque ligne de manière appropriée. **PR_DEPTH** est de base zéro ; les lignes dont la valeur est 0 dans leur colonne **PR_DEPTH** ne sont pas mises en retrait. Plus la valeur de **PR_DEPTH** est élevée, plus la ligne est mise en retrait. Par exemple, les lignes avec **PR_DEPTH** définies sur 1 sont mises en retrait d’un onglet, tandis que les lignes avec **PR_DEPTH** définies sur 3 sont mises en retrait de trois onglets. 
  
 **PR_SELECTABLE** est utilisé pour indiquer si une ligne du tableau représente un modèle qui peut être sélectionné et utilisé pour créer un destinataire. Bien que la plupart des lignes d’une table unique représentent des modèles, les fournisseurs peuvent inclure des lignes autres que des lignes de modèle. Par exemple, un fournisseur peut souhaiter organiser la table unique par type de modèle, y compris une ligne de catégorie qui apparaît dans l’affichage, mais qui n’est pas utilisée pour la création du destinataire. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

