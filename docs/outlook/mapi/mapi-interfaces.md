---
title: Interfaces MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346682"
---
# <a name="mapi-interfaces"></a>Interfaces MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La documentation de chaque interface est constituée d'une section introductive qui contient une brève description de l'objectif de l'interface, suivie d'un tableau contenant les informations suivantes.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Fichier d'en-tête dans lequel l'interface est définie et qui doit être incluse lorsque vous compilez votre code source.  <br/> |
|Exposé par:  <br/> |Objet qui expose l'interface.  <br/> |
|Implémenté par :  <br/> |Liste des composants qui fournissent une implémentation de l'interface.  <br/> |
|Appelé par :  <br/> |Liste des composants qui appellent généralement les méthodes de l'interface.  <br/> |
|Identificateur de l'interface:  <br/> |GUID de l'identificateur de l'interface.  <br/> |
|Type de pointeur:  <br/> |Type de pointeur pour l'objet qui expose l'interface.  <br/> |
|Modèle de transaction:  <br/> |Pour les interfaces dérivées de [IMAPIProp](imapipropiunknown.md). Si elles ne sont pas effectuées, les modifications prennent effet immédiatement; en cas de transaction, les modifications ne prennent effet que si [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) est appelé.  <br/> |
   
Le premier tableau est un autre tableau répertoriant toutes les méthodes de cette interface dans l'ordre vtable. Un vtable est un tableau de pointeurs de fonction créés par le compilateur et contenant un pointeur de fonction pour chaque méthode d'un objet MAPI. Les méthodes sont répertoriées dans l'ordre dans lequel elles sont déclarées. Les méthodes héritées d'autres interfaces ne sont pas affichées dans la table de commandes vtable, mais peuvent être utilisées de la même manière que dans l'interface qui les définit.
  
Après chaque rubrique de l'interface, les méthodes de l'interface sont ensuite documentées par ordre alphabétique. Pour chaque méthode, la documentation inclut une instruction succincte, un bloc de syntaxe et les informations suivantes.
  
|**Titre**|**Content**|
|:-----|:-----|
|Paramètres  <br/> |Une description de chaque paramètre dans la méthode.  <br/> |
|Valeur de retour  <br/> |Description des valeurs uniques que la méthode peut renvoyer. Il s'agit des valeurs que les appelants doivent vérifier dans leur code.  <br/> |
|Remarques  <br/> |Une description de la raison et de la façon dont la méthode est utilisée.  <br/> |
|Voir aussi  <br/> |Renvois à d'autres rubriques de cette référence.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Référence MAPI](mapi-reference.md)

