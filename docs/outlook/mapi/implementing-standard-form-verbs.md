---
title: Mise en œuvre de verbes de formulaire standard
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a85a3adcd2fab920e9cbbd39bdd7a5ad52f223db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600833"
---
# <a name="implementing-standard-form-verbs"></a>Mise en œuvre de verbes de formulaire standard

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit un ensemble de verbes standard, ou actions entreprises lorsqu’un utilisateur effectue une sélection de menu ou clique sur un bouton, que toutes les visionneuses de formulaire doivent prendre en charge. Chaque verbe est associé à une constante pour l’identification, définie dans l’EXCHFORM. Fichier d’en-tête H. Le tableau suivant répertorie les verbes de formulaire standard et leurs constantes associées :
  
|**Verb**|**Valeur**|
|:-----|:-----|
|Ouvrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Répondre  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Répondre à tous  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Transférer  <br/> |EXCHIVERB_FORWARD  <br/> |
|Imprimer  <br/> |EXCHIVERB_PRINT  <br/> |
|Enregistrer sous  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Répondre dans le fichier  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Lorsqu’un utilisateur choisit un verbe, passez sa constante dans un appel à la méthode [IMAPIForm::D oVerb](imapiform-doverb.md) du formulaire pour effectuer son action correspondante. 
  
En plus d’accéder aux verbes via votre visionneuse de formulaires, les utilisateurs peuvent parfois accéder aux verbes directement à partir du formulaire. Par exemple, certains objets de formulaire  permettent à l’utilisateur d’appeler le  verbe Imprimer en cliquant avec le bouton droit sur le formulaire et en choisissant Imprimer à partir d’un menu contextuelle. 
  

