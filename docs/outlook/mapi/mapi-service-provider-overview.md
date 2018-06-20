---
title: Vue d’ensemble du fournisseur de services MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 15a53a0bb16db3683e4c1320ac2e54648c8c697b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784704"
---
# <a name="mapi-service-provider-overview"></a>Vue d’ensemble du fournisseur de services MAPI

  
  
**S’applique à**: Outlook 
  
Entre le sous-système MAPI et les systèmes de messagerie sont les fournisseurs de services différents. Fournisseurs de services sont comme pilotes qui se connectent les applications clientes MAPI à un système de messagerie sous-jacent. Il existe trois types de fournisseurs : message banque, carnet d’adresses ou répertoire fournisseurs et les fournisseurs de transport de messages. MAPI prend en charge chaque type de service autonome, l’activation d’un fournisseur à proposer un ou plusieurs fournisseurs de services personnalisés. Par exemple, un fournisseur souhaiterez pour créer un fournisseur de carnet d’adresses qui utilise un répertoire de l’annuaire d’entreprise d’employés ou pour créer un fournisseur de magasin de message qui utilise une base de données.
  
Fournisseurs de services sont généralement écrites pour les systèmes de messagerie spécifiques par les développeurs de logiciels qui ont des connaissances spécialisées ou d’expérience avec un système donné. Par exemple, les Services de Microsoft Outlook 2010 mobiles Microsoft Outlook 2013 utilisent un fournisseur de carnet d’adresses pour exposer un carnet d’adresses du téléphone mobile dans Outlook. 
  
MAPI présente les applications clientes avec une vue unifiée des informations du fournisseur de transport et le carnet d’adresses. Cette approche intégrée empêche l’application cliente d’avoir à mapper les données sur le fournisseur approprié. Elle empêche également l’utilisateur de devoir négocier entre plusieurs carnet d’adresses et modèles d’adressage fournisseur de transport. Informations de fournisseur de magasin de message, toutefois, ne sont pas unifiées et les clients qui utilisent plusieurs fournisseurs de banque de messages sont chargés de leur traitement individuellement.
  
Utiliser les fournisseurs de services MAPI pour créer et envoyer des messages de la manière suivante : les messages sont créés à l’aide d’un formulaire qui est approprié pour le type spécifique, ou la classe de message. Nombre de messages est effectuée avec le formulaire note standard qui est fourni avec le sous-système MAPI, soit par l’utilisateur d’une application cliente ou par programme sans intervention de l’utilisateur. Le message terminé est adressé à un ou plusieurs destinataires — un utilisateur ou un groupe d’utilisateurs désignés pour recevoir le message. Un destinataire peut ou peuvent ne pas avoir une entrée dans un répertoire parmi les fournisseurs de carnet d’adresses installé possède. Les destinataires qui ne sont pas associés à un fournisseur de carnet d’adresses installées sont appelées destinataires personnalisés ou des adresses uniques. Une adresse unique peut être temporaire, une durée jusqu'à ce que le message est envoyé. 
  
Lorsque l’application cliente envoie le message, le fournisseur de banque de message vérifie que chaque destinataire possède une adresse valide et unique et que le message a toutes les informations nécessaires pour la transmission. S’il existe une question sur un destinataire (par exemple, lorsqu’il y a plusieurs destinataires portant le même nom), un fournisseur de carnet d’adresses prend en charge de la résolution de l’ambiguïté. Le message est alors placé dans la file d’attente sortante. 
  
## <a name="see-also"></a>Voir aussi



[Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

