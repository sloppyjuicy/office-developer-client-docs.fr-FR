---
title: Accès au code XLL dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accéder au code xll [Excel 2007], XLL [Excel 2007] accéder au code, commandes [Excel 2007], inscription, fonctions [Excel 2007], inscription, appel des XLL à partir d’Excel, inscription de commandes [Excel 2007], inscription de fonctions [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: 9f228432da71e406bbff40d760bc3dd38d5d4ee3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593018"
---
# <a name="accessing-xll-code-in-excel"></a>Accès au code XLL dans Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Pour être accessibles dans Microsoft Excel, les fonctions et les commandes contenues dans un XLL :
  
- doivent être exportées par le XLL ;
    
- doivent être inscrites avec Excel.
    
## <a name="registering-functions-and-commands-with-excel"></a>Inscription de fonctions et de commandes avec Excel

L’inscription indique à Excel les points suivants concernant un point d’entrée DLL :
  
- S’il est masqué ou, s’il s’agit d’une fonction, si elle est visible dans l’Assistant Fonction.
    
- S’il peut être appelé uniquement à partir d’une feuille macro XLM ou à partir d’une feuille de calcul également.
    
- S’il s’agit d’une commande, si c’est une fonction de feuille de calcul ou une fonction équivalente à une feuille macro.
    
- Son nom d’exportation XLL/DLL et le nom qu’Excel doit utiliser.
    
- S’il s’agit d’une fonction :
    
  - Quels types de données elle renvoie et prend comme arguments.
    
  - Si elle renvoie son résultat en modifiant un argument en place.
    
  - Si elle est volatile.
    
  - Si elle est thread-safe (pris en charge à partir d’Excel 2007).
    
  - Le texte que l’Assistant Coller une fonction et l’éditeur de saisie semi-automatique doivent afficher pour appeler la fonction.
    
  - Sous quelle catégorie de fonction elle doit être répertoriée.
    
Tout ceci est réalisé à l’aide de la fonction API C [xlfRegister](xlfregister-form-1.md), équivalente à la fonction XLM **REGISTER**.
  
## <a name="calling-xll-functions-directly-from-excel"></a>Appel des fonctions XLL directement à partir d’Excel

Une fois qu’elles sont inscrites, les fonctions de feuille de calcul et de feuille macro XLL peuvent être appelées de tout emplacement d’où une fonction intégrée peut être appelée :
  
- Une formule à cellule unique ou de tableau sur une feuille de calcul.
    
- Une formule à cellule unique ou de tableau sur une feuille macro.
    
- La définition d’un nom défini.
    
- Les champs de condition et de limite dans une boîte de dialogue de mise en forme conditionnelle.
    
- À partir d’un autre complément via la fonction API C [xlUDF](xludf.md).
    
- À partir de Visual Basic for Applications (VBA) via la méthode **Application.Run**. 
    
Vous pouvez obtenir une référence à la cellule ou à la plage de cellules d’appel dans votre fonction à l’aide de la fonction API C **xlfCaller**. Si la fonction a été appelée à partir de l’expression de mise en forme conditionnelle de la cellule, une référence à la cellule ou aux cellules associée(s) vous est renvoyée, donc vous ne pouvez pas considérer que la formule de la cellule contient la fonction XLL. Si votre fonction a été appelée à partir d’une fonction VBA définie par l’utilisateur (UDF), **xlfCaller** renvoie l’adresse des cellules qui ont appelé la fonction VBA. Pour plus d'informations, consultez [xlfCaller](xlfcaller.md).
  
> [!NOTE]
> Excel appelle également le code de fonction XLL à partir de l’**Assistant Coller une fonction** et des boîtes de dialogue **Remplacer**. Vous devrez peut-être restreindre l’exécution normale de votre code dans le cas de la boîte de dialogue des **arguments Coller une fonction**, notamment lorsque l’exécution de votre fonction peut être longue. Pour détecter si votre fonction est appelée à partir de ces boîtes de dialogue, vous devez implémenter du code dans votre projet qui se reproduit dans toutes les fenêtres ouvertes pour déterminer si la première fenêtre est l’une de ces boîtes de dialogue et, si c’est le cas, laquelle. 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Appel de commandes XLL directement à partir d’Excel

Une fois qu’elles sont inscrites, les commandes XLL peuvent être appelées à l’aide de toutes les autres méthodes utilisées pour appeler d’autres macros définies par l’utilisateur :
  
- En les associant à un objet de contrôle incorporé sur une feuille de calcul.
    
- À partir de la boîte de dialogue Exécuter une macro.
    
- À partir d’une macro définie par l’utilisateur VBA à l’aide la méthode **Application.Run**. 
    
- À partir d’un élément de menu personnalisé ou de la barre d’outils.
    
- À l’aide d’une combinaison de touches de définie lors de l’inscription de la commande.
    
- En tant que commande à exécuter lorsqu’un événement spécifié est bloqué.
    
> [!NOTE]
> Les commandes XLL sont masquées dans le sens où elles n’apparaissent pas dans la liste des macros disponibles dans les boîtes de dialogue Excel. Cependant, elles peuvent être entrées manuellement dans le champ du nom de la macro. Dans Excel, le nom sous lequel la commande a été inscrite doit être entré dans ces boîtes de dialogue, et non le nom d’exportation DLL. 
  
Toutes les commandes XLL inscrites avec Excel sont considérées par Excel comme étant de la forme suivante :
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

Excel ignore la valeur de renvoi, sauf si elle est appel�e � partir d�une feuille macro XLM, auquel cas la valeur de retour est convertie en **TRUE** ou **FALSE**. Vous devez par cons�quent renvoyer 1 si votre commande a �t� ex�cut�e correctement, et 0 si elle a �chou� ou a �t� annul�e par l�utilisateur.
  
Vous pouvez obtenir des informations sur la manière dont votre commande a été appelée à l’aide de la fonction API C **xlfCaller**. Pour plus d'informations, consultez [xlfCaller](xlfcaller.md).
  
À partir d’Excel 2007, l’interface utilisateur est très différente des versions antérieures. Les fonctions API C qui autorisent l’ajout et la suppression de barres de menus, menus, sous-menus, éléments de menu, barres d’outils et boutons de barre d’outils personnalisés sont toujours prises en charge dans la plupart des cas. Toutefois, il se peut qu’elles ne rendent pas toujours disponible l’élément ajouté de la même façon que ce à quoi vos utilisateurs sont habitués. Vous devez vérifier soigneusement que toute fonction ajoutée est toujours accessible, ou implémenter une personnalisation propre à la version. À partir d’Excel 2007, l’interface utilisateur est mieux personnalisée à l’aide d’un module de code managé qui peut être étroitement associé à vos commandes XLL.
  
## <a name="see-also"></a>Voir aussi

- [Création de XLL](creating-xlls.md)
- [Appel des fonctions XLL à partir de l’Assistant Fonction ou des boîtes de dialogue Remplacer](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)
- [Développement de XLL de Excel](developing-excel-xlls.md)



