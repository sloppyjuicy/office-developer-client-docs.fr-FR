---
title: Interfaces MAPI
description: Fournit une description détaillée de la façon dont la documentation pour les interfaces MAPI et leurs propriétés associées sont structurées.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
ms.openlocfilehash: 46da72a67527cc0ba9707b1be1c0b1156e8f3521
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812747"
---
# <a name="mapi-interfaces"></a>Interfaces MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La documentation de chaque interface se compose d’une section d’introduction qui inclut une brève description de l’objectif de l’interface, suivie d’un tableau contenant les informations suivantes.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Fichier d’en-tête dans lequel l’interface est définie et qui doit être inclus lorsque vous compilez votre code source. |
|Exposé par :  <br/> |Objet qui expose l’interface. |
|Implémenté par :  <br/> |Liste des composants qui fournissent une implémentation de l’interface. |
|Appelé par :  <br/> |Liste des composants qui appellent généralement les méthodes de l’interface. |
|Identificateur d’interface :  <br/> |GUID de l’identificateur d’interface. |
|Type de pointeur :  <br/> |Type de pointeur pour l’objet qui expose l’interface. |
|Modèle de transaction :  <br/> |Pour les interfaces dérivées [d’IMAPIProp](imapipropiunknown.md). S’il n’est pas traité, les modifications prennent effet immédiatement ; si les modifications sont traitées, les modifications ne prennent effet qu’après l’appel [d’IMAPIProp::SaveChanges](imapiprop-savechanges.md) . |
   
Après la première table se trouve une autre table qui répertorie toutes les méthodes de cette interface dans l’ordre des tables virtuelles. Une table virtuelle est un tableau de pointeurs de fonction créé par le compilateur contenant un pointeur de fonction pour chaque méthode d’un objet MAPI. Les méthodes sont répertoriées dans le même ordre qu’elles sont déclarées. Les méthodes héritées d’autres interfaces ne sont pas affichées dans la table Order de table de tables virtuelles, mais peuvent être utilisées de la même façon que celles documentées dans l’interface qui les définit.
  
Après chaque rubrique d’interface, les méthodes de l’interface sont ensuite documentées par ordre alphabétique. Pour chaque méthode, la documentation inclut une brève instruction à usage, un bloc de syntaxe et les informations suivantes.
  
|**Titre**|**Content**|
|:-----|:-----|
|Paramètres  <br/> |Description de chaque paramètre de la méthode. |
|Valeur de retour  <br/> |Description des valeurs uniques que la méthode peut retourner. Il s’agit des valeurs que les appelants doivent rechercher dans leur code. |
|Remarques  <br/> |Description du pourquoi et de la façon dont la méthode est utilisée. |
|Voir aussi  <br/> |Références croisées à d’autres rubriques de cette référence. |
   
## <a name="see-also"></a>Voir aussi



[Référence MAPI](mapi-reference.md)

