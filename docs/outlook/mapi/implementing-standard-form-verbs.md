---
title: Implémentation de verbes formulaire Standard
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8135af7947f30ac600b8d9af364b2a79a3443ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784200"
---
# <a name="implementing-standard-form-verbs"></a>Implémentation de verbes formulaire Standard

  
  
**S’applique à**: Outlook 
  
MAPI définit un ensemble de verbes standard ou les actions effectuées lorsqu’un utilisateur effectue une sélection de menu ou clique sur un bouton, toutes les visionneuses de formulaire doivent prendre en charge. Chaque verbe possède une constante associée à l’identification, définie dans le EXCHFORM. Fichier d’en-tête H. Le tableau suivant répertorie les verbes formulaire standard et les constantes associées :
  
|**Verbe**|**Valeur**|
|:-----|:-----|
|Ouvrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Répondre  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Répondre à tous  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Transférer  <br/> |EXCHIVERB_FORWARD  <br/> |
|Imprimer  <br/> |EXCHIVERB_PRINT  <br/> |
|Enregistrer en tant que  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Répondre à un dossier  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Lorsqu’un utilisateur choisit un verbe, transmettez la constante dans un appel à la méthode du formulaire [IMAPIForm::DoVerb](imapiform-doverb.md) pour effectuer son action correspondante. 
  
En plus de l’accès à des verbes via votre visionneuse de formulaire, les utilisateurs peuvent accéder parfois verbes directement à partir du formulaire. Par exemple, certains objets formulaire autorise l’utilisateur à appeler le verbe **Imprimer** en avec le bouton droit sur le formulaire et en choisissant **Imprimer** dans un menu contextuel. 
  

