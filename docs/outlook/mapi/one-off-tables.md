---
title: Tables ponctuelles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439526"
---
# <a name="one-off-tables"></a>Tables ponctuelles

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table ponctuelle contient des informations sur les modèles pris en charge par un fournisseur de carnet d'adresses pour la création de nouveaux destinataires. Les tables ponctuelles sont implémentées par des fournisseurs de carnet d'adresses, des conteneurs de carnet d'adresses individuels et par MAPI, et peuvent être permanentes ou temporaires. 
  
> [!NOTE]
> Ne confondez pas les modèles dans les tables ponctuelles avec des identificateurs de modèle; Bien que leurs objectifs soient similaires, leurs constructions de code ne sont pas similaires. Les modèles sont utilisés pour créer des destinataires d'un type particulier tandis que les identificateurs de modèle sont utilisés pour lier les données d'un destinataire qui appartiennent à un fournisseur d'hôte avec du code afin de prendre en charge un autre destinataire appartenant à un fournisseur étranger. 
  
Les clients créent des destinataires:
  
- Ajouter à la liste des destinataires d'un message sortant.
    
- À ajouter à l'un des conteneurs dans le carnet d'adresses.
    
Dans les deux cas, un fournisseur de carnets d'adresses est invité à renvoyer une table ponctuelle. Les fournisseurs de carnet d'adresses peuvent implémenter une seule table unique à utiliser dans les deux situations ou une table ponctuelle unique pour chaque situation. 
  
Lorsque le destinataire est inclus dans un message sortant, MAPI appelle la méthode [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) du fournisseur de carnet d'adresses pour récupérer sa table One-Off. La table ponctuelle inclut des modèles qui permettent à un utilisateur d'entrer des informations résultant de la création d'un destinataire avec une adresse valide. MAPI s'inscrit pour les notifications de cette table, le laissant s'ouvrir afin que les modifications puissent être répercutées sur l'utilisateur. MAPI ne libère la table que lorsque la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) de son sous-système ou de son carnet d'adresses est appelée. 
  
Lorsque le destinataire est ajouté à un conteneur, MAPI effectue un autre appel en appelant la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur pour extraire sa propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). L'ensemble de modèles inclus dans cette table One-Off représente les types de destinataires qui peuvent être ajoutés au conteneur. Par exemple, les serveurs de messagerie exposent souvent un conteneur pour chaque passerelle installée de sorte que chaque conteneur ne contienne que des adresses spécifiques à la passerelle correspondante.
  
MAPI fournit une table ponctuelle qui inclut ses propres modèles, ainsi que les modèles de chacun des fournisseurs de carnet d'adresses de la session. MAPI fournit un modèle générique qui peut être utilisé pour créer un nouveau destinataire pour n'importe quel type d'adresse, en supposant que l'utilisateur connaisse son format. Les fournisseurs de carnets d'adresses utilisent ce tableau isolé en appelant [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md). Chacun des modèles inclus dans la table ponctuelle MAPI entraîne la création de destinataires avec des adresses de destinataire valides.
  
Les fournisseurs de carnets d'adresses fournissent généralement un modèle pour chaque type d'adresse qu'ils prennent en charge. Toutefois, la prise en charge des modèles n'est pas obligatoire. Les fournisseurs de carnet d'adresses qui n'autorisent pas la création de nouvelles adresses peuvent renvoyer MAPI_E_NO_SUPPORT lorsque MAPI appelle pour demander une table ponctuelle. Les fournisseurs de carnet d'adresses qui permettent la création d'adresses mais ne fournissent pas de modèles peuvent appeler **IMAPISupport:: GetOneOffTable** pour utiliser les modèles figurant dans la table ponctuelle MAPI. 
  
Les propriétés suivantes constituent le jeu de colonnes obligatoire dans les tables ponctuelles:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indique le type d'adresse qui peut être associé au nouveau destinataire créé avec le modèle. 
  
 **PR_DISPLAY_NAME** et **PR_DISPLAY_TYPE** associent les données au nouveau destinataire. **PR_DISPLAY_NAME** contient une chaîne de caractères qui identifie le nouveau destinataire et **PR_DISPLAY_TYPE** contient une constante qui identifie le type d'icône à afficher avec la ligne. Les modèles pour les utilisateurs de messagerie ont leur colonne **PR_DISPLAY_TYPE** définie sur DT_MAILUSER; les modèles pour les listes de distribution ont leur colonne **PR_DISPLAY_TYPE** définie sur DT_DISTLIST. 
  
 **PR_ENTRYID** est l'identificateur d'entrée du modèle à utiliser pour créer un destinataire. Cet identificateur d'entrée peut être passé aux futures [IAddrBook:: NewEntry](iaddrbook-newentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md)et [IABContainer:: CreateEntry](iabcontainer-createentry.md) appels. Les conteneurs définissent la colonne **PR_ENTRYID** de leur ligne pour le modèle utilisateur de messagerie par défaut sur **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et la colonne **PR_ENTRYID** de leur ligne pour la liste de distribution par défaut. modèle à **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** est utilisé pour prendre en charge l'affichage hiérarchique des entrées dans un tableau isolé en indiquant le niveau de retrait du modèle. Bien que les tables ponctuelles puissent être affichées sous la forme d'une liste plate ou d'un affichage hiérarchique, le dernier est préférable et les fournisseurs de carnets d'adresses doivent le prendre en charge en définissant la colonne **PR_DEPTH** pour chaque ligne de façon appropriée. **PR_DEPTH** est de base zéro; les lignes avec une valeur de 0 dans leur colonne **PR_DEPTH** ne sont pas mises en retrait. Plus la valeur est élevée ****, plus la ligne est mise en retrait. Par exemple, les lignes avec **PR_DEPTH** défini sur 1 sont mises en retrait d'un onglet tandis que les lignes avec **PR_DEPTH** définies sur 3 sont mises en retrait de trois onglets. 
  
 **PR_SELECTABLE** est utilisé pour indiquer si une ligne du tableau représente un modèle qui peut être sélectionné et utilisé pour créer un destinataire. Bien que la plupart des lignes d'une table ponctuelle représentent des modèles, les fournisseurs peuvent inclure des lignes qui ne sont pas des modèles. Par exemple, un fournisseur peut souhaiter organiser le tableau One-off par type de modèle, y compris une ligne de catégorie qui apparaît dans l'affichage, mais qui n'est pas utilisée pour la création de destinataires. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

