---
title: À propos des chaînes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Les formules peuvent contenir des chaînes. Pour mettre en forme une chaîne, dans une cellule de message, une valeur d’élément de données de forme ou un champ, par exemple, vous devez définir un modèle de format. Le résultat peut être formaté sous forme de paire nombre-unité, de chaîne, de date-heure, de durée ou d’unité monétaire. Par exemple, le format picture0 #/10 uuformats les paires nombre-unité de 2 AS10 9/10 centimètres.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345065"
---
# <a name="about-strings"></a><span data-ttu-id="1c1bf-106">À propos des chaînes</span><span class="sxs-lookup"><span data-stu-id="1c1bf-106">About Strings</span></span>

<span data-ttu-id="1c1bf-p102">Les formules peuvent contenir des chaînes. Pour mettre en forme une chaîne, dans une cellule de message, une valeur d’élément de données de forme ou un champ, par exemple, vous devez définir un modèle de format. Le résultat peut être formaté sous forme de paire nombre-unité, de chaîne, de date-heure, de durée ou d’unité monétaire. Par exemple, le modèle de format « 0 #/10 uu » affiche la paire nombre-unité 10,9cm sous la forme « 10 9/10 centimètres ».</span><span class="sxs-lookup"><span data-stu-id="1c1bf-p102">Formulas can contain strings. To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture. Output can be formatted as a number-unit pair, string, date-time, duration, or currency. For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="1c1bf-111">Vous pouvez utiliser les images de format dans la cellule **format** de la section données de forme et en tant qu'argument de la fonction **format** ou **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="1c1bf-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="1c1bf-112">Lorsque vous insérez un champ de texte, les modèles s’affichent dans la liste des formats de la boîte de dialogue **Champ** (onglet **Insertion**).</span><span class="sxs-lookup"><span data-stu-id="1c1bf-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="1c1bf-113">Utilisation de fonctions pour mettre en forme des chaînes</span><span class="sxs-lookup"><span data-stu-id="1c1bf-113">Using functions to format strings</span></span>

<span data-ttu-id="1c1bf-114">Dans toute formule qui est résolue en chaîne, y compris les formules de champ de texte personnalisé, vous pouvez utiliser la fonction **format** ou **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="1c1bf-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="1c1bf-115">La fonction FORMAT renvoie une chaîne mise en forme.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="1c1bf-116">La fonction **FORMATEX** convertit une entrée non typée en unités choisies pour le résultat mis en forme.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="1c1bf-117">Affichage des données de forme mises en forme</span><span class="sxs-lookup"><span data-stu-id="1c1bf-117">Displaying formatted shape data</span></span>

<span data-ttu-id="1c1bf-118">Vous pouvez mettre en forme la valeur affichée d’un élément de données de forme en indiquant un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="1c1bf-p105">Par exemple, une forme de planning peut être associée à un élément de données de forme permettant de mesurer le coût d’un processus. Par défaut, un élément de données de forme est une chaîne. Pour mettre en forme la chaîne « 1200 », vous pouvez entrer « ### ###,00 € » dans la cellule Format pour afficher le symbole monétaire.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-p105">For example, a project timeline shape can have a shape data item that measures the cost of a process. By default, a shape data item value is a string. To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="1c1bf-122">Microsoft Visio utilise les paramètres de l’onglet **Devise** dans la boîte de dialogue **Personnaliser le format** de l’élément **Région et langue** du Panneau de configuration pour déterminer le symbole monétaire et le séparateur des milliers à afficher.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="1c1bf-123">(Dans **le panneau de configuration**, cliquez sur **région et langue**, puis cliquez sur **paramètres supplémentaires**.)</span><span class="sxs-lookup"><span data-stu-id="1c1bf-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="1c1bf-124">Pour convertir une chaîne en valeur monétaire afin d’effectuer des calculs, utilisez la fonction CY.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="1c1bf-125">Utilisation de fonctions pour manipuler des chaînes de texte</span><span class="sxs-lookup"><span data-stu-id="1c1bf-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="1c1bf-p107">Vous pouvez utiliser des fonctions pour manipuler des chaînes de texte, par exemple, pour rechercher ou remplacer certains caractères dans une chaîne de texte. Il est également possible d’obtenir des informations concernant la position d’un caractère dans une chaîne ou d’identifier les caractères de début et de fin d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-p107">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string. You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

