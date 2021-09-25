---
title: Interfaces MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b8d0fb625270422eb1910154afcada906b8dccd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610285"
---
# <a name="mapi-interfaces"></a>Interfaces MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La documentation de chaque interface se compose d’une section d’introduction qui inclut une brève description de l’objectif de l’interface, suivie d’un tableau contenant les informations suivantes.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Fichier d’en-tête dans lequel l’interface est définie et qui doit être inclus lorsque vous compilez votre code source.  <br/> |
|Exposé par :  <br/> |Objet qui expose l’interface.  <br/> |
|Implémenté par :  <br/> |Liste des composants qui fournissent une implémentation de l’interface.  <br/> |
|Appelé par :  <br/> |Liste des composants qui appellent généralement les méthodes de l’interface.  <br/> |
|Identificateur d’interface :  <br/> |GUID de l’identificateur d’interface.  <br/> |
|Type de pointeur :  <br/> |Type de pointeur pour l’objet qui expose l’interface.  <br/> |
|Modèle de transaction :  <br/> |Pour les interfaces dérivées [d’IMAPIProp](imapipropiunknown.md). Si ce n’est pas le cas, les modifications prennent effet immédiatement ; si elles sont transposées, les modifications ne prennent effet [qu’une fois IMAPIProp::SaveChanges](imapiprop-savechanges.md) appelé.  <br/> |
   
Le premier tableau suivant est un autre tableau qui répertorie toutes les méthodes de cette interface dans l’ordre vtable. Un tableau vtable est un tableau de pointeurs de fonction créé par le compilateur contenant un pointeur de fonction pour chaque méthode d’un objet MAPI. Les méthodes sont répertoriées dans le même ordre qu’elles sont déclarées. Les méthodes héritées d’autres interfaces ne sont pas affichées dans la table Order Vtable, mais peuvent être utilisées de la même manière que dans l’interface qui les définit.
  
Après chaque rubrique d’interface, les méthodes de l’interface sont ensuite documentées par ordre alphabétique. Pour chaque méthode, la documentation inclut une brève instruction à usage, un bloc de syntaxe et les informations suivantes.
  
|**Titre**|**Content**|
|:-----|:-----|
|Paramètres  <br/> |Description de chaque paramètre de la méthode.  <br/> |
|Valeur de retour  <br/> |Description des valeurs uniques que la méthode peut renvoyer. Voici les valeurs que les appelants doivent vérifier dans leur code.  <br/> |
|Remarques  <br/> |Description du pourquoi et de la façon dont la méthode est utilisée.  <br/> |
|Voir aussi  <br/> |Renvois à d’autres rubriques de cette référence.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Référence MAPI](mapi-reference.md)

