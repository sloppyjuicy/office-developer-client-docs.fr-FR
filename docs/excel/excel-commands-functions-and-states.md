---
title: Commandes, fonctions et états Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- États [excel 2007], [Excel 2007] de commandes, fonctions de feuille de calcul [Excel 2007], les fonctions de feuille macro [Excel 2007], États Excel
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782048"
---
# <a name="excel-commands-functions-and-states"></a>Commandes, fonctions et états Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel reconnaît deux types de nouvelles fonctionnalités très différents : les fonctions et les commandes.
  
## <a name="commands"></a>Commandes

Dans Excel, les commandes ont les caractéristiques suivantes :
  
- Ils permettent d’actions de la même manière que les utilisateurs.
    
- Ils peuvent faire tout ce qu’un utilisateur peut faire (sujet aux limites de l’interface utilisée), telles que la modification des paramètres d’Excel, l’ouverture, fermeture et modifier des documents, lancement recalculs et ainsi de suite.
    
- Elles peuvent être définies à appeler lorsque certains événements interceptées se produisent.
    
- Ils peuvent afficher des boîtes de dialogue et interagir avec l’utilisateur.
    
- Ils peuvent être liés pour contrôler des objets afin qu’ils sont appelées lors de certaines actions sur cet objet, telles que clic gauche.
    
- Ils ne sont jamais appelés par Excel pendant le recalcul.
    
- Elles ne peut pas être appelées par les fonctions pendant un nouveau calcul.
    
## <a name="functions"></a>Fonctions

Fonctions d’Excel procédez comme suit :
  
- Ils prennent généralement des arguments et renvoient toujours un résultat.
    
- Ils peuvent être saisis dans une ou plusieurs cellules en tant que partie d’une formule Excel.
    
- Ils peuvent être utilisés dans les définitions de nom défini.
    
- Ils peuvent être utilisés dans la limite de mise en forme conditionnelle et d’expressions de seuil.
    
- Ils peuvent être appelées par les commandes.
    
- Ils ne peuvent pas appeler des commandes.
    
Excel établit une distinction supplémentaire entre les fonctions de feuille de calcul défini par l’utilisateur et des fonctions définies par l’utilisateur sont conçues pour fonctionner dans des feuilles macro. Excel ne limite pas les fonctions de feuille macro définie par l’utilisateur uniquement à utilisé dans les feuilles de macro : ces fonctions peuvent être utilisées n’importe où une fonction de feuille de calcul normale peut être utilisée.
  
### <a name="worksheet-functions"></a>Objet Worksheet Functions

Vous trouverez ci-dessous des fonctions de feuille de calcul Excel :
  
- Ils ne peut pas accéder aux fonctions d’information de feuille de macro.
    
- Ils ne peuvent pas obtenir les valeurs des cellules non calculées.
    
- Ils peuvent être écrites et enregistrés en tant que thread-safe à compter d’Excel 2007.
    
### <a name="macro-sheet-functions"></a>Fonctions de feuille macro

Vous trouverez ci-dessous des fonctions de feuille macro Excel :
  
- Ils peuvent accéder des fonctions d’information feuille macro.
    
- Ils peuvent obtenir les valeurs des cellules non calculées, y compris les valeurs des cellules d’appel.
    
- Ils ne sont pas considérées thread fiables à compter d’Excel 2007.
    
Comment Excel traite une fonction définie par l’utilisateur (UDF), ce qui permet la fonction faire et comment il recalcule la fonction sont déterminés tout lorsque vous enregistrez la fonction. Si une fonction est enregistrée comme une fonction de feuille de calcul mais tente de faire quelque chose que seule une fonction de feuille macro, l’opération échoue. À compter d’Excel 2007, si une fonction de feuille de calcul enregistrée en tant que thread-safe tente d’appeler une fonction de feuille macro, là encore, l’opération échoue.
  
Excel traite Microsoft Visual Basic pour Applications (VBA) UDF en tant que fonctions équivalent de la feuille de macro, dans la mesure où ils peuvent accéder aux informations de l’espace de travail et la valeur de cellules non calculées, et ils ne sont pas considérées comme thread fiables à compter d’Excel 2007.
  
## <a name="excel-states"></a>États Excel

Excel peut être dans un des différents États à un moment donné en fonction des actions de l’utilisateur, un processus externe, un événement interceptée exécutant une macro ou un événement de maintenance Excel chronométré comme **enregistrement automatique**.
  
Les états possibles d’une expérience de l’utilisateur sont les suivantes :
  
- **Prêt état :** Aucun commandes ou des macros ne sont en cours d’exécution. Aucune boîte de dialogue n’est affichés. Aucune cellule n’est en cours de modification et l’utilisateur n’est pas au milieu d’une opération de couper/copier et coller. Aucun objet incorporé n’a le focus. 
    
- **En mode édition :** L’utilisateur a commencé à taper les caractères d’entrée valides dans une cellule déverrouillée ou non protégée, ou a appuyé sur **F2** sur une ou plusieurs cellules déverrouillées ou non protégées. 
    
- **Mode Couper/copier et coller :** L’utilisateur a Couper ou copier une cellule ou plage de cellules et n’a pas encore collé les ou a collée à l’aide de la boîte de dialogue Collage spécial qui permet à plusieurs opérations de collage. 
    
- **En mode point :** L’utilisateur modifie une formule et sélectionne les cellules dont les adresses sont ajoutés à la formule en cours de modification. 
    
L’utilisateur peut désactiver le mode édition, point et couper/copier en appuyant sur la touche **ÉCHAP** , ce qui rétablit l’état prêt Excel. Autres événements peuvent désactiver ces États, telles que les suivantes : 
  
- L’utilisateur ouvre une boîte de dialogue intégrée.
    
- L’utilisateur lance un nouveau calcul.
    
- L’utilisateur exécute une commande.
    
- Excel effectue une opération **d’enregistrement** . 
    
- Un événement de minuterie est intercepté.
    
L’exemple précédent est important pour complément aux développeurs. Vous devez tenir compte l’impact de l’utilisation d’Excel où événement timer fréquents intercepte normale est définie et exécutée. Lorsqu’il s’agit d’une part importante de la fonctionnalité de votre complément, vous devez fournir aux utilisateurs un moyen de suspension, afin qu’ils puissent couper/copier et coller normalement lorsqu’ils ont besoin de facilement accessible.
  
## <a name="see-also"></a>Voir aussi



[Concepts de programmation Excel](excel-programming-concepts.md)
  
[Autorisation utilisateur sauts dans les opérations de longue durée](permitting-user-breaks-in-lengthy-operations.md)

