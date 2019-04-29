---
title: Implémentation de verbes de formulaire standard
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426120"
---
# <a name="implementing-standard-form-verbs"></a>Implémentation de verbes de formulaire standard

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit un ensemble de verbes standard, ou actions effectuées lorsqu'un utilisateur effectue une sélection de menu ou clique sur un bouton, que tous les visiteurs de formulaire doivent prendre en charge. Chaque verbe a une constante associée à l'identification, définie dans le EXCHFORM. Fichier d'en-tête H. Le tableau suivant répertorie les verbes de formulaire standard et les constantes qui leur sont associées:
  
|**Verb**|**Valeur**|
|:-----|:-----|
|Ouvrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Répondre  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Répondre à tous  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Transférer  <br/> |EXCHIVERB_FORWARD  <br/> |
|Print  <br/> |EXCHIVERB_PRINT  <br/> |
|Enregistrer sous  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Répondre dans le fichier  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Lorsqu'un utilisateur choisit un verbe, transmettez sa constante dans un appel à la méthode [IMAPIForm du formulaire::D overb](imapiform-doverb.md) pour effectuer l'action correspondante. 
  
Outre l'accès à des verbes via la visionneuse de formulaire, les utilisateurs peuvent parfois accéder à des verbes directement à partir du formulaire. Par exemple, certains objets Form permettent à l'utilisateur d'appeler le verbe **Print** en cliquant avec le bouton droit sur le formulaire et en sélectionnant **Print** à partir d'un menu contextuel. 
  

