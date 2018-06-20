---
title: Accès au code XLL dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accès au code xll [excel 2007], XLL [Excel 2007], accès au code, commandes [Excel 2007], inscription, fonctions [Excel 2007], l’enregistrement, l’appel XLL à partir d’Excel, inscription commandes [Excel 2007], enregistrement de fonctions [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782014"
---
# <a name="accessing-xll-code-in-excel"></a>Accès au code XLL dans Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Pour être accessibles dans Microsoft Excel, les fonctions et les commandes qui contient un XLL :
  
- Doivent être exportées par la XLL.
    
- Doit être enregistré avec Excel.
    
## <a name="registering-functions-and-commands-with-excel"></a>Inscription des fonctions et les commandes dans Excel

Enregistrement indique à Excel ce qui suit sur un point d’entrée DLL :
  
- Si elle est masquée ou, si une fonction, si elle est visible dans l’Assistant fonction.
    
- Il est ou non être appelée uniquement à partir d’une feuille de macro XLM ou à partir d’une feuille de calcul.
    
- Si une commande, si elle est une fonction de feuille de calcul ou une fonction équivalents de feuille macro.
    
- Quel est son nom d’exportation DLL ou XLL et le nom que vous souhaitez utiliser.
    
- S’il s’agit d’une fonction :
    
  - Quelles données types de retours et prend comme arguments.
    
  - Si elle renvoie son résultat en modifiant un argument en place.
    
  - Si elle est volatile.
    
  - Si elle est thread-safe (commençant pris en charge dans Excel 2007).
    
  - Quel éditeur de saisie semi-automatique et de l’Assistant fonction Coller de texte doivent s’afficher pour contribuer à l’appel de la fonction.
    
  - Fonction catégorie, qu'elle doit être répertoriée sous.
    
Tout cela à l’aide de l’API C fonction [xlfRegister](xlfregister-form-1.md), équivalente à la fonction XLM **inscrire**.
  
## <a name="calling-xll-functions-directly-from-excel"></a>Appel de fonctions XLL directement à partir d’Excel

Une fois qu’ils sont enregistrés, fonctions de feuille de macro et de feuille de calcul XLL peuvent être appelées à partir de n’importe où de qu'une fonction intégrée peut être appelée à partir :
  
- Une formule de cellule unique ou un tableau dans une feuille de calcul.
    
- Une formule de cellule unique ou un tableau dans une feuille macro.
    
- La définition d’un nom défini.
    
- Les champs condition et limite dans une boîte de dialogue Mise en forme conditionnelle.
    
- À partir d’un autre complément par le biais de l’API C fonctionner [xlUDF](xludf.md).
    
- À partir de Visual Basic pour Applications (VBA) via la méthode **application.Run appropriée** . 
    
Vous pouvez obtenir une référence à la cellule ou plage de cellules appelant au sein de votre fonction à l’aide de la fonction de API C **xlfCaller**. Si la fonction a été appelée à partir de l’expression de mise en forme conditionnelle de la cellule, vous revenez toujours une référence à la cellule associée ou les cellules, afin que vous ne pouvez pas supposer que la formule de cellule contient la fonction XLL. Si la fonction a été appelée à partir d’une fonction définie par l’utilisateur VBA (UDF), **xlfCaller** renvoie à nouveau l’adresse des cellules qui a appelé la fonction VBA. Pour plus d’informations, voir [xlfCaller](xlfcaller.md).
  
> [!NOTE]
> Excel appelle également le code de la fonction XLL dans les boîtes de dialogue **Assistant fonction de collage** et **Remplacer** . Vous devrez peut-être restreindre de votre code normal en cours d’exécution dans le cas de la boîte de dialogue **Arguments de la fonction Coller** , en particulier où votre fonction peut prendre beaucoup de temps à exécuter. Pour détecter si votre fonction est appelée à partir d’une de ces boîtes de dialogue, vous devez implémenter du code dans votre projet qui parcourt toutes les fenêtres ouvertes pour déterminer si la fenêtre frontal est une de ces boîtes de dialogue et, le cas échéant, laquelle. 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Appeler des commandes XLL directement à partir d’Excel

Une fois qu’ils sont enregistrés, commandes XLL peuvent être appelées dans toutes les méthodes que les autres macros définies par l’utilisateur peuvent être appelées :
  
- Par associé à un objet de contrôle incorporé dans une feuille de calcul.
    
- Dans la boîte de dialogue Exécuter une Macro.
    
- À partir d’une macro VBA définies par l’utilisateur à l’aide de la méthode **Application.Run** . 
    
- À partir d’un élément de menu personnalisé ou une barre d’outils.
    
- À l’aide d’une séquence de touches de raccourci définie lors de l’inscription de la commande.
    
- La commande à exécuter lorsqu’un événement spécifié est interceptée.
    
> [!NOTE]
> Commandes XLL sont masquées en ce sens qu’ils n’apparaissent pas dans la liste des macros disponibles dans les boîtes de dialogue Excel. Mais ils peuvent être entrés manuellement dans le champ nom de macro. Excel suppose que le nom enregistré en tant que ces boîtes de dialogue, pas le nom d’exportation de la DLL. 
  
Toutes les commandes XLL auprès d’Excel sont utilisés par Microsoft Excel pour être sous la forme suivante :
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

[!REMARQUE] Excel ignore la valeur de renvoi, sauf si elle est appel�e � partir d�une feuille macro XLM, auquel cas la valeur de retour est convertie en **TRUE** ou **FALSE**. Vous devez par cons�quent renvoyer 1 si votre commande a �t� ex�cut�e correctement, et 0 si elle a �chou� ou a �t� annul�e par l�utilisateur.
  
Vous pouvez obtenir des informations sur la façon dont votre commande a été appelée à l’aide de l’API C fonctionner **xlfCaller**. Pour plus d’informations, voir [xlfCaller](xlfcaller.md).
  
À compter d’interface utilisateur d’Excel 2007 est très différent des versions antérieures. Les fonctions API C qui autorisent l’ajout et la suppression des barres de menus, menus, sous-menus, éléments de menu, barres d’outils personnalisées et des boutons de barre d’outils sont toujours pris en charge la plupart des cas. Toutefois, ils peuvent toujours faites pas l’élément ajouté disponibles d’une manière qui connaissent vos utilisateurs. Vous devez vérifier avec soin que toute fonctionnalité ajoutée est toujours accessible ou implémenter une personnalisation spécifique à la version. Démarrage de l’interface utilisateur dans Excel 2007 mieux personnalisé à l’aide d’un module de code managé qui peut ensuite être étroitement à vos commandes XLL.
  
## <a name="see-also"></a>Voir aussi

- [Cr�ation de XLL](creating-xlls.md)
- [Appel des fonctions XLL à partir de l’Assistant fonction ou remplacer des boîtes de dialogue](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)
- [D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)



