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
description: Formules peuvent contenir des chaînes. Mise en forme la chaîne de sortie, comme dans une cellule de message, une élément de données de forme ou un champ de texte, vous spécifiez un format de l’image. Sortie peut être mis en forme comme une paire nombre-unité, chaîne, date-heure, de durée ou de devise. Par exemple, l’uuformats de 10/format picture0 l’unité de nombre paire 10,9 cm as10 9/10 centimètres.
ms.openlocfilehash: 1fd003ecd5c824042e97a40fa8374aeead254ddc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787981"
---
# <a name="about-strings"></a><span data-ttu-id="19643-106">À propos des chaînes</span><span class="sxs-lookup"><span data-stu-id="19643-106">About Strings</span></span>

<span data-ttu-id="19643-p102">Les formules peuvent contenir des chaînes. Pour mettre en forme une chaîne, dans une cellule de message, une valeur d’élément de données de forme ou un champ, par exemple, vous devez définir un modèle de format. Le résultat peut être formaté sous forme de paire nombre-unité, de chaîne, de date-heure, de durée ou d’unité monétaire. Par exemple, le modèle de format « 0 #/10 uu » affiche la paire nombre-unité 10,9cm sous la forme « 10 9/10 centimètres ».</span><span class="sxs-lookup"><span data-stu-id="19643-p102">Formulas can contain strings. To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture. Output can be formatted as a number-unit pair, string, date-time, duration, or currency. For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="19643-111">Vous pouvez utiliser des modèles de format dans la cellule **Format** de la section données de forme et en tant qu’argument à la fonction **FORMAT** ou **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="19643-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="19643-112">Lorsque vous insérez un champ de texte, les modèles s’affichent dans la liste des formats de la boîte de dialogue **champ** (onglet**Insertion** ).</span><span class="sxs-lookup"><span data-stu-id="19643-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="19643-113">Utilisation des fonctions de chaînes de format</span><span class="sxs-lookup"><span data-stu-id="19643-113">Using functions to format strings</span></span>

<span data-ttu-id="19643-114">Dans une formule qui est résolue en une chaîne, y compris les formules de champ de texte personnalisé, vous pouvez utiliser la fonction **FORMAT** ou **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="19643-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="19643-115">La fonction FORMAT renvoie une chaîne mise en forme.</span><span class="sxs-lookup"><span data-stu-id="19643-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="19643-116">La fonction **FORMATEX** convertit sans type pour les unités que vous choisissez pour le résultat de la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="19643-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="19643-117">Affichage des données de forme mises en forme</span><span class="sxs-lookup"><span data-stu-id="19643-117">Displaying formatted shape data</span></span>

<span data-ttu-id="19643-118">Vous pouvez mettre en forme la valeur affichée d’un élément de données de forme en indiquant un modèle de format dans la cellule Format.</span><span class="sxs-lookup"><span data-stu-id="19643-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="19643-p105">Par exemple, une forme de planning peut être associée à un élément de données de forme permettant de mesurer le coût d’un processus. Par défaut, un élément de données de forme est une chaîne. Pour mettre en forme la chaîne « 1200 », vous pouvez entrer « ### ###,00 € » dans la cellule Format pour afficher le symbole monétaire.</span><span class="sxs-lookup"><span data-stu-id="19643-p105">For example, a project timeline shape can have a shape data item that measures the cost of a process. By default, a shape data item value is a string. To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="19643-122">Microsoft Visio utilise les paramètres sous l’onglet **devise** dans la boîte de dialogue **Personnaliser le Format** de l’élément de **langue et région** dans le panneau de configuration pour déterminer le symbole monétaire et milliers séparateur à afficher.</span><span class="sxs-lookup"><span data-stu-id="19643-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="19643-123">(Dans **Le panneau de configuration**, cliquez sur la **langue et région**, puis cliquez sur **Paramètres supplémentaires**.)</span><span class="sxs-lookup"><span data-stu-id="19643-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="19643-124">Pour convertir une chaîne en valeur monétaire afin d’effectuer des calculs, utilisez la fonction CY.</span><span class="sxs-lookup"><span data-stu-id="19643-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="19643-125">Utilisation des fonctions pour manipuler des chaînes de texte</span><span class="sxs-lookup"><span data-stu-id="19643-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="19643-p107">Vous pouvez utiliser des fonctions pour manipuler des chaînes de texte, par exemple, pour rechercher ou remplacer certains caractères dans une chaîne de texte. Il est également possible d’obtenir des informations concernant la position d’un caractère dans une chaîne ou d’identifier les caractères de début et de fin d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="19643-p107">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string. You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

