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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ca3752e8f7e910994811dec85cc2f1b00e184661
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584807"
---
# <a name="mapi-interfaces"></a>Interfaces MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La documentation de chaque interface se compose d’une section d’introduction qui inclut une brève description de l’objectif de l’interface suivie d’une table qui contient les informations suivantes.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Le fichier d’en-tête dans laquelle l’interface est définie et qui doit être inclus lorsque vous compilez votre code source.  <br/> |
|Exposés par :  <br/> |L’objet qui expose l’interface.  <br/> |
|Implémentée par :  <br/> |Une liste des composants qui fournissent une implémentation de l’interface.  <br/> |
|Appelée par :  <br/> |Une liste des composants qui appellent généralement les méthodes de l’interface.  <br/> |
|Identificateur de l’interface :  <br/> |L’identificateur GUID d’interface.  <br/> |
|Type de pointeur :  <br/> |Le type de pointeur de l’objet qui expose l’interface.  <br/> |
|Modèle de transaction :  <br/> |Pour les interfaces dérivées de [IMAPIProp](imapipropiunknown.md). Si nontransacted, les modifications prennent effet immédiatement. Si le traitement modifications ne prendront effet qu’après [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée.  <br/> |
   
La première table est un autre tableau qui répertorie toutes les méthodes de cette interface dans l’ordre vtable. Une vtable est un tableau de pointeurs fonction créé par le compilateur contenant un pointeur de fonction pour chaque méthode d’un objet MAPI. Les méthodes sont répertoriées dans le même ordre qu’elles sont déclarées. Méthodes héritées d’autres interfaces ne sont pas affichées dans le tableau de l’ordre Vtable, mais peuvent être utilisées de la même manière comme indiqué dans l’interface qui définit les.
  
Après chaque rubrique interface, les méthodes de l’interface sont documentées puis par ordre alphabétique. Pour chaque méthode, la documentation inclut une instruction brève objectif, un bloc de syntaxe et les informations suivantes.
  
|**Titre**|**Content**|
|:-----|:-----|
|Paramètres  <br/> |Une description de chaque paramètre de la méthode.  <br/> |
|Valeur renvoyée  <br/> |Description de la méthode peut renvoyer les valeurs uniques. Voici les valeurs que les appelants doivent vérifier dans leur code.  <br/> |
|Remarques  <br/> |Description de pourquoi et comment la méthode est utilisée.  <br/> |
|Voir aussi  <br/> |Références croisées à d’autres rubriques dans cette référence.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[R�f�rence MAPI (en anglais)](mapi-reference.md)

