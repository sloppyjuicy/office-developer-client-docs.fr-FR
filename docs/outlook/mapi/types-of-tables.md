---
title: Types de tables
description: Décrit différents types de tables, chaque type différencié par les informations qu’il présente, dans Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
ms.openlocfilehash: c1b39a778155acf97786495ceec8c86a5ac9d906
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894046"
---
# <a name="types-of-tables"></a>Types de tables

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreux types de tables différents, chaque type étant différencié par les informations qu’il présente. Les tables permettent aux applications clientes et aux fournisseurs de services d’accéder facilement aux propriétés importantes de nombreux types d’objets et de les manipuler. 
  
Certaines tables, telles que les tables de contenu, offrent une autre façon d’accéder aux propriétés. Par exemple, un client peut récupérer l’objet d’un message (sa propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) directement à partir du message en appelant sa méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ou via la table de contenu du message. D’autres tables fournissent le seul moyen d’accéder aux propriétés de l’objet. Par exemple, un client ne peut pas accéder à la propriété **PR_ATTACH_METHOD** d’une pièce jointe ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) en appelant **IMAPIProp::GetProps** ; il doit toujours récupérer la table de pièces jointes du message auquel il est attaché. **PR_ATTACH_METHOD** est une colonne obligatoire dans toutes les tables de pièces jointes. 
  
Une vue de table peut être statique ou dynamique. Avec une vue de table statique, les modifications apportées aux données sous-jacentes n’entraînent pas la mise à jour de la vue. Une fois la vue instanciée, elle ne change pas. Les utilisateurs de tables statiques peuvent être informés des modifications apportées aux données par le biais de notifications de table. Une vue de table dynamique est mise à jour lorsque des modifications sont apportées aux données. Il existe deux types de tables dynamiques : une qui met à jour les colonnes de chaque ligne, mais les lignes restent statiques et l’autre qui met à jour les colonnes et les lignes. Ce dernier type de table reflète toujours exactement les données sous-jacentes.
  
Les tables ont un ensemble de colonnes par défaut, l’ensemble minimal de colonnes qu’un client ou un fournisseur de services peut s’attendre à voir lors de la récupération de lignes à partir d’une table qui n’a pas encore été affectée par un appel [IMAPITable::SetColumns](imapitable-setcolumns.md) . Les clients et les fournisseurs de services peuvent ajouter ou supprimer des colonnes de cet ensemble par défaut en appelant la méthode **SetColumns** . Les modifications peuvent être apportées de manière statique ou dynamique, à la suite d’une demande du client. Toutes les tables ne prennent pas en charge la modification dynamique des ensembles de colonnes. 
  
Les tables MAPI et leurs implémenteurs et utilisateurs sont les suivants :
  
|**Tableau**|**Implémenteurs**|
|:-----|:-----|
|Pièce jointe  <br/> |Implémenté par les fournisseurs de magasin de messages. Utilisé par les clients et les fournisseurs de transport. |
|Sommaire  <br/> |Implémenté par le magasin de messages et les fournisseurs de carnets d’adresses. Utilisé par les clients. |
|Afficher  <br/> |Implémenté par MAPI et les fournisseurs de services. Utilisé par MAPI et les fournisseurs de services. |
|Hierarchy  <br/> |Implémenté par le magasin de messages et les fournisseurs de carnets d’adresses. Utilisé par les clients. |
|Service de message  <br/> |Implémenté par MAPI. Utilisé par les clients. |
|Magasin de messages  <br/> |Implémenté par MAPI. Utilisé par les clients. |
|Une seule fois  <br/> |Implémenté par les fournisseurs de carnets d’adresses. Utilisé par MAPI. |
|File d’attente sortante  <br/> |Implémenté par les fournisseurs de magasin de messages. Utilisé par le spouleur MAPI. |
|Profils  <br/> |Implémenté par MAPI. Utilisé par les clients. |
|Fournisseur  <br/> |Implémenté par MAPI. Utilisé par les clients. |
|Dossier de r�ception  <br/> |Implémenté par les fournisseurs de magasin de messages. Utilisé par les clients. |
|Destinataire  <br/> |Implémenté par les fournisseurs de magasin de messages. Utilisé par les clients et les fournisseurs de transport. |
|Statut  <br/> |Implémenté par MAPI et les fournisseurs de services. Utilisé par les clients. |
   
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

