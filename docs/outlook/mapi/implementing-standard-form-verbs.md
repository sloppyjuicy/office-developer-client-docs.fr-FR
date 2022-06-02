---
title: Implémentation de verbes de formulaire standard
description: MAPI définit un ensemble de verbes standard ou d’actions effectuées lorsqu’un utilisateur effectue une sélection de menu ou clique sur un bouton.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
ms.openlocfilehash: cca7e44b3bddf3421591e31ec217aec38b5a82a3
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828417"
---
# <a name="implementing-standard-form-verbs"></a>Implémentation de verbes de formulaire standard

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit un ensemble de verbes standard, ou des actions effectuées lorsqu’un utilisateur effectue une sélection de menu ou clique sur un bouton, que tous les visionneuses de formulaires doivent prendre en charge. Chaque verbe a une constante associée pour l’identification, définie dans EXCHFORM. Fichier d’en-tête H. Le tableau suivant répertorie les verbes de formulaire standard et leurs constantes associées :
  
|**Verb**|**Valeur**|
|:-----|:-----|
|Ouvrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Répondre  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Répondre à tous  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Transférer  <br/> |EXCHIVERB_FORWARD  <br/> |
|Imprimer  <br/> |EXCHIVERB_PRINT  <br/> |
|Enregistrer sous  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Répondre dans le fichier  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Lorsqu’un utilisateur choisit un verbe, transmettez sa constante dans un appel à la méthode [IMAPIForm::D oVerb](imapiform-doverb.md) du formulaire pour effectuer son action correspondante. 
  
En plus d’accéder aux verbes via votre visionneuse de formulaires, les utilisateurs peuvent parfois accéder aux verbes directement à partir du formulaire. Par exemple, certains objets de formulaire permettent à l’utilisateur d’appeler le verbe **Imprimer** en cliquant avec le bouton droit sur le formulaire et en choisissant **Imprimer** à partir d’un menu contextuel. 
  

