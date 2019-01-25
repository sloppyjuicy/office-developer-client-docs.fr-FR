---
title: États, fonctions et commandes Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- états [Excel 2007], commandes [Excel 2007], fonctions de feuille de calcul [Excel 2007], fonctions de feuille macro [Excel 2007], états Excel
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716235"
---
# <a name="excel-commands-functions-and-states"></a>États, fonctions et commandes Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel reconnaît deux types de fonctionnalités ajoutées très différents : les commandes et les fonctions.
  
## <a name="commands"></a>Commandes

Dans Excel, les commandes présentent les caractéristiques suivantes :
  
- Elles effectuent des actions de la même façon que les utilisateurs.
    
- Elles peuvent faire tout ce qu’un utilisateur peut faire (dans les limites de l’interface utilisée) : changer des paramètres Excel, ouvrir, fermer et modifier des documents, démarrer des recalculs, etc.
    
- Elles peuvent être configurées pour être appelées lorsque certains événements bloqués se produisent.
    
- Elles peuvent afficher des boîtes de dialogue et interagir avec l’utilisateur.
    
- Elles peuvent être liées pour contrôler des objets afin d’être appelées lorsqu’une action est effectuée sur cet objet (clic gauche, par exemple).
    
- Elles ne sont jamais appelés par Excel lors d’un recalcul.
    
- Elle ne peuvent pas être appelées par des fonctions lors d’un recalcul.
    
## <a name="functions"></a>Fonctions

Les fonctions dans Excel présentent les caractéristiques suivantes :
  
- Elles prennent généralement des arguments et renvoient toujours un résultat.
    
- Elles peuvent être entrées dans une ou plusieurs cellules dans une formule Excel.
    
- Elles peuvent être utilisées dans des définitions de nom défini.
    
- Elles peuvent être utilisées dans la limite de mise en forme conditionnelle et les expressions de seuil.
    
- Elles peuvent être appelées par des commandes.
    
- Elles ne peuvent pas appeler de commandes.
    
Excel fait une distinction supplémentaire entre les fonctions de feuille de calcul définies par l’utilisateur et les fonctions définies par l’utilisateur qui sont conçues pour fonctionner sur des feuilles macro. Excel ne limite pas les fonctions de feuille macro définies par l’utilisateur uniquement à une utilisation sur des feuilles macro : ces fonctions peuvent être utilisées partout où une fonction de feuille de calcul normale peut être utilisée.
  
### <a name="worksheet-functions"></a>Fonctions de feuille de calcul

Les fonctions de feuille de calcul Excel présentent les caractéristiques suivantes :
  
- Elles ne peuvent pas accéder aux fonctions d’informations de feuille macro.
    
- Elles ne peuvent pas obtenir les valeurs de cellules non calculées.
    
- Elles peuvent être écrites et inscrites comme thread-safe à partir d’Excel 2007.
    
### <a name="macro-sheet-functions"></a>Fonctions de feuille macro

Les fonctions de feuille macro Excel présentent les caractéristiques suivantes :
  
- Elles peuvent accéder aux fonctions d’informations de feuille macro.
    
- Elles peuvent obtenir les valeurs de cellules non calculées, y compris les valeurs des cellules d’appel.
    
- Elles ne sont pas considérées comme thread-safe à partir d’Excel 2007.
    
C’est au moment où vous inscrivez la fonction que sont déterminés tous les éléments suivants : comment Excel traite une fonction définie par l’utilisateur (UDF), ce qu’il autorise la fonction à faire et comment il recalcule la fonction. Si une fonction est inscrite comme fonction de feuille de calcul mais qu’elle tente de faire quelque chose que seule une feuille macro peut faire, l’opération échoue. À partir d’Excel 2007, si une fonction de feuille de calcul inscrite comme thread-safe tente d’appeler une fonction de feuille macro, là encore, l’opération échoue.
  
Excel traite les fonctions définies par l’utilisateur Microsoft Visual Basic for Applications (VBA) comme des fonctions équivalentes aux fonctions de feuilles macro. En effet, elles peuvent accéder aux informations d’espace de travail et à la valeur de cellules non calculées, et ne sont pas considérées comme thread-safe à partir d’Excel 2007.
  
## <a name="excel-states"></a>États Excel

Excel peut être dans de nombreux états à un moment donné, selon les actions de l’utilisateur, un processus externe, un événement bloqué exécutant une macro ou un événement de maintenance interne Excel chronométré comme **Autosave**.
  
Les états de l’utilisateur sont les suivants :
  
- **Prêt :** Aucune commande ni macro n’est en cours d’exécution. Aucune boîte de dialogue n’est affichée. Aucune cellule n’est en cours de modification et l’utilisateur n’est pas au milieu d’une opération couper/copier et coller. Aucun objet incorporé n’est utilisé. 
    
- **Mode Édition :** L’utilisateur a commencé à taper des caractères d’entrée valides dans une cellule déverrouillée ou non protégée ou a utilisé la touche **F2** sur une ou plusieurs cellules déverrouillées ou non protégées. 
    
- **Mode Couper/copier et coller :** L’utilisateur a coupé ou copié une cellule ou une plage de cellules et ne l’a pas encore collée ou l’a collée en utilisant la boîte de dialogue Collage spécial, qui permet plusieurs opérations de collage. 
    
- **Mode Pointer :** L’utilisateur modifie une formule et sélectionne des cellules dont les adresses sont ajoutées à la formule en cours de modification. 
    
L’utilisateur peut effacer les modes Édition, Pointer et Couper/copier en appuyant sur la touche **Échap**. Excel revient dans l’état Prêt. D’autres événements peuvent effacer ces états, tels que : 
  
- L’utilisateur ouvre une boîte de dialogue prédéfinie.
    
- L’utilisateur lance un recalcul.
    
- L’utilisateur exécute une commande.
    
- Excel effectue une opération **Autosave** (enregistrement automatique). 
    
- Un événement de minuteur est bloqué.
    
Le dernier exemple est important pour les développeurs de compléments. Vous devez tenir compte de l’impact de l’utilisation d’Excel normale lorsque des captures d’événement de minuteur fréquentes sont définies et exécutées. Lorsqu’il s’agit d’une partie importante des fonctionnalités de votre complément, vous devez fournir aux utilisateurs un moyen facilement accessible de l’interrompre pour qu’ils puissent couper/copier et coller normalement lorsqu’ils en ont besoin.
  
## <a name="see-also"></a>Voir aussi



[Concepts de programmation Excel](excel-programming-concepts.md)
  
[Autorisation des interruptions utilisateur lors des opérations très longues](permitting-user-breaks-in-lengthy-operations.md)

