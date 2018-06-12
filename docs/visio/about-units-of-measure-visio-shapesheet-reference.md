---
title: À propos des unités de mesure (référence Visio ShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251828
localization_priority: Normal
ms.assetid: 48f765a8-7485-03c0-3484-d4ec07822600
description: Lorsque vous insérez des champs dans du texte ou construisez des formules, vous devez souvent indiquer l’unité de mesure des valeurs que vous tapez.
ms.openlocfilehash: ce8ad1cdcbdaba713edeb06f4cd949e49f82a311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788002"
---
# <a name="about-units-of-measure-visio-shapesheet-reference"></a>À propos des unités de mesure (référence Visio ShapeSheet)

Lorsque vous insérez des champs dans du texte ou construisez des formules, vous devez souvent indiquer l’unité de mesure des valeurs que vous tapez.
  
Microsoft Visio évalue le résultat d’une formule différemment selon la cellule dans laquelle vous entrez la formule. En règle générale, les cellules qui représentent la position de la forme, une dimension ou un angle nécessitent une paire nombre-unité qui se compose d’un nombre et l’unité nécessaires pour interpréter le nombre. Nombre de cellules ne requièrent des unités et correspondre à une chaîne, à la valeur TRUE ou FALSE ou à un index. Par exemple, la même formule dans la cellule **FillForegnd** , indique la couleur 5 dans la palette de couleurs signifie que la valeur TRUE (et verrouille la largeur de la forme) dans la cellule LockWidth. 
  
Veillez à toujours indiquer une unité de mesure lorsque vous entrez une formule dans une cellule devant contenir une cote. Si vous ne précisez pas d’unité de mesure, Visio utilise l’unité par défaut pour cette cellule, qui peut être une unité de page, de dessin ou d’angle.
  
## <a name="units-of-measure"></a>Unités de mesure

Dans les formules ShapeSheet, entrez les unités de mesure en utilisant les abréviations présentées dans le tableau suivant.
  
|**Pour indiquer ces unités de mesure**|**Utiliser**|**Constante d’Automation**|
|:-----|:-----|:-----|
| Centimètres  <br/> | cm  <br/> |**visCentimeters (69)** <br/> |
| Cicéros  <br/> | c  <br/> |**visCiceros (54)** <br/> |
| Date ou heure  <br/> | date  <br/> |**visDate (40)** <br/> |
| Degrés  <br/> | deg  <br/> |**valeur visDegrees (81)** <br/> |
| Didots  <br/> | d  <br/> |**visDidots (53)** <br/> |
| Semaines écoulées  <br/> | se.  <br/> |**visElapsedWeek (43)** <br/> |
| Jours écoulés  <br/> | je.  <br/> |**valeur visElapsedDay (44)** <br/> |
| Heures écoulées  <br/> | he.  <br/> |**visElapsedHour (45)** <br/> |
| Minutes écoulées  <br/> | me.  <br/> |**valeur visElapsedMin (46)** <br/> |
| Secondes écoulées  <br/> | se.  <br/> |**valeur visElapsedSec (47)** <br/> |
| Pieds  <br/> | pi  <br/> |**visFeet (66)** <br/> |
| Pouces  <br/> | po  <br/> |**visInches (65)** <br/> |
| Kilomètres  <br/> | km  <br/> |**visKilometers (72)** <br/> |
| Mètres  <br/> | m  <br/> |**visMeters (71)** <br/> |
| Miles  <br/> | mi  <br/> |**visMiles (68)** <br/> |
| Millimètres  <br/> | mm  <br/> |**visMillimeters (70)** <br/> |
| Minutes  <br/> | '  <br/> |**visMin (84)** <br/> |
| Milles nautiques  <br/> | nm  <br/> |**visNautMiles (76)** <br/> |
| Pourcentage  <br/> | %  <br/> |**visPercent (33)** <br/> |
| Picas  <br/> | p  <br/> |**visPicas (51)** <br/> |
| Points  <br/> | pt  <br/> |**visPoints (50)** <br/> |
| Radians  <br/> | rad  <br/> |**valeur visRadians (83)** <br/> |
| Secondes  <br/> | "  <br/> |**visSec (85)** <br/> |
| Yards  <br/> | yd  <br/> |**visYards (75)** <br/> |
   
## <a name="compound-units-of-measure"></a>Unités de mesure composées

Dans les formules, vous pouvez exprimer des unités de mesure pour les nombres composés à l’aide des abréviations dans le tableau suivant. Visio simplifie les résultats et les affiche dans les unités composées.
  
Par exemple, si vous entrez 45,635 °, Visio affiche la valeur équivalente en tant que 45° 38' 6 " ».
  
|**Pour définir les unités**|**Utilisez cette abréviation**|**Constante d’Automation**|
|:-----|:-----|:-----|
| Cicéros et didots  <br/> | CICERO/DIDOT  <br/> |**visCicerosAndDidots (52)** <br/> |
| Degrés, minutes et secondes  <br/> | °  <br/> |**visDegreeMinSec (82)** <br/> |
| Pieds et pouces  <br/> | PIEDS/POUCE  <br/> |**visFeetAndInches (67)** <br/> |
| Picas et points  <br/> | PICAPOINTS  <br/> |**visPicasAndPoints (49)** <br/> |
   
## <a name="fractional-units-of-measure"></a>Unités de mesure en fraction

Vous pouvez spécifier les unités de mesure en fraction dans la cellule **DrawingScale** à affecter le nombre de graduations de la règle que Visio affiche dans la fenêtre de dessin. Par défaut, Visio divise les distances en dixième lors de ses règles de dessin. Si vous utilisez des unités de mesure en fraction dans la cellule **DrawingScale** , Visio divise les éléments suivants : 
  
- Huitièmes pour *visInchFrac* et *visMileFrac* 
    
- Douzièmes pour *visFeetAndInches* 
    
Les unités de mesure en fraction n’ont aucun effet dans les cellules autres que DrawingScale.
  
|**Pour spécifier des unités en fraction**|**Utilisez cette abréviation**|**Constante d’Automation**|
|:-----|:-----|:-----|
| Pouces avec leurs divisions  <br/> | IN_F  <br/> |**visInchFrac (73)** <br/> |
| Miles avec leurs divisions  <br/> | MI_F  <br/> |**visMileFrac (74)** <br/> |
| Pieds et pouces  <br/> | PIEDS/POUCE  <br/> |**visFeetAndInches (67)** <br/> |
   
## <a name="multidimensional-units-of-measure"></a>Unités de mesure multidimensionnelles

Dans les formules, vous pouvez exprimer des unités de mesure pour les nombres multidimensionnels à l’aide des abréviations du tableau suivant. Visio simplifie les résultats et les affiche dans les unités multidimensionnelles.
  
|**Pour définir des unités multidimensionnelles**|**Utilisez cette abréviation**|**Constante d’Automation**|
|:-----|:-----|:-----|
| Acre  <br/> | ACRES  <br/> |**visAcre (36)** <br/> |
| Centimètres  <br/> | CM. CARRE, CM CARRE, CM.^2, CM^2  <br/> |**visCentimeters (69)** <br/> |
| Pieds  <br/> | PI. CARRE, PI CARRE, PIEDS^2, PI^2  <br/> |**visFeet (66)** <br/> |
| Hectare  <br/> | HECTARES, HECTARE, HA., HA  <br/> |**visHectare (37)** <br/> |
| Pouces  <br/> | PO. CARRE, PO CARRE, POUCES^2, PO^2  <br/> |**visInches (65)** <br/> |
| Kilomètres  <br/> | KM. CARRE, KM CARRE, KM.^2, KM ^2  <br/> |**visKilometers (72)** <br/> |
| Mètres  <br/> | M. CARRE, M CARRE, M.^2, M ^2  <br/> |**visMeters (71)** <br/> |
| Miles  <br/> | MI. CARRE, MI CARRE, MI.^2, MI ^2  <br/> |**visMiles (68)** <br/> |
| Millimètres  <br/> | MM. CARRE, MM CARRE, MM.^2, MM ^2  <br/> |**visMillimeters (70)** <br/> |
| Yards  <br/> | YD. CARRE, YD CARRE, YD.^2, YD^2  <br/> |**visYards (75)** <br/> |
   
## <a name="universal-strings"></a>Chaînes universelles

Dans les versions localisées de Visio, les chaînes reconnues changent en fonction de la langue utilisée. Si vous souhaitez travailler avec plusieurs langues, utilisez les chaînes universelles pour les unités de mesure.
  
|**Pour**|**Utiliser**|
|:-----|:-----|
| Centimètres  <br/> | CM  <br/> |
| Cicéros  <br/> | C  <br/> |
| Cicéros et didots  <br/> | CICERO/DIDOT  <br/> |
| Date ou heure  <br/> | DATE  <br/> |
| Degrés  <br/> | DEG  <br/> |
| Degrés, minutes, secondes  <br/> | °  <br/> |
| Didots  <br/> | D  <br/> |
| Semaine écoulée  <br/> | EW  <br/> |
| Jour écoulé  <br/> | ED  <br/> |
| Heure écoulée  <br/> | EH  <br/> |
| Minute écoulée  <br/> | EM  <br/> |
| Seconde écoulée  <br/> | ES  <br/> |
| Pieds  <br/> | FT  <br/> |
| Pieds et pouces  <br/> | PIEDS/POUCE  <br/> |
| Pouces  <br/> | IN  <br/> |
| Pouces avec leurs divisions  <br/> | IN_F  <br/> |
| Kilomètres  <br/> | KM  <br/> |
| Mètres  <br/> | M  <br/> |
| Miles  <br/> | MI  <br/> |
| Miles avec leurs divisions  <br/> | MI_F  <br/> |
| Millimètres  <br/> | MM  <br/> |
| Minutes  <br/> | '  <br/> |
| Milles nautiques  <br/> | NM  <br/> |
| Pour cent  <br/> | %  <br/> |
| Picas  <br/> | P  <br/> |
| Picas et points  <br/> | PICAPOINTS  <br/> |
| Points  <br/> | PT  <br/> |
| Radians  <br/> | RAD  <br/> |
| Secondes  <br/> | "  <br/> |
| Yards  <br/> | YD  <br/> |
   
## <a name="implicit-units-of-measure"></a>Unités de mesure implicites

Lorsque Visio analyse et stocke une paire nombre-unité, il peut utiliser des unités explicites ou implicites. Un nombre exprimé en unité explicite s’affiche toujours dans l’unité de mesure entrée à l’origine. Un nombre exprimé en unité implicite est toujours converti en une valeur équivalente dans l’unité de dessin, de page ou d’angle spécifique à la cellule.
  
Supposons que vous entriez l’équivalent de 1 pouce dans la cellule A en utilisant une unité explicite et dans la cellule B avec une unité implicite et que ces deux cellules utilisent des unités de dessin. Vous remplacez ensuite l’unité par défaut de la page par des centimètres. La cellule A affiche toujours 1 pouce car elle utilise une unité explicite non modifiée par l’unité par défaut. En revanche, la cellule B affiche désormais 2,54 cm, soit la valeur équivalente dans l’unité par défaut.
  
Pour entrer des unités implicitement, utilisez la syntaxe suivante.
  
```vb
number  [unit , flag ]
```

|||
|:-----|:-----|
| _number_ <br/> |Valeur d’origine, telle que 3,7, 1,7E-4 ou 5 1/2.  <br/> |
| _unité_ <br/> |Unités dans lesquelles le _nombre_ est initialement exprimé.  <br/> |
| _indicateur_ <br/> |Système de mesure à utiliser lorsque l’unité de valeur implicite est affichée. Reportez-vous au tableau ci-dessous.  <br/> |
   
paramètre _indicateur_ est une des lettres suivantes (majuscules ou minuscules) indiquant le système de mesure qui doit être utilisé lorsque l’unité de valeur implicite est affichée. 
  
|**_Indicateur_**|**Système de mesure**|**Exemple**|
|:-----|:-----|:-----|
| a, A  <br/> | Angle  <br/> | =5[deg,A]  <br/> |
| d, D  <br/> | Dessin  <br/> | =5[in,D]  <br/> |
| e, E  <br/> | Durée  <br/> | =5[eh,E]  <br/> |
| p, P  <br/> | Page  <br/> | =5[in,P]  <br/> |
| t, T  <br/> | Type  <br/> | =5[pt,T]  <br/> |
   
En outre, vous pouvez utiliser les unités implicites DL, DP, DT, DA, DE pour implicite dessin, page, texte-, angulaire- et unité de temps, respectivement. Ces unités supposent que la valeur associée est unités internes. Par exemple, si le système de mesure en cours utilise les centimètres, *= 2 DL* être interprété comme 2 unités internes (pouces) et affiché sous la forme 5,08 cm. 
  
Dans la syntaxe des unités implicites décrite ci-dessus, cette expression (=2 DL) est équivalente à 2[in,d]. Elle a l’avantage de vous laisser le choix des valeurs, ce qui vous permet d’indiquer par exemple 2[ft,d], interprété comme 2 pieds et affiché ainsi : 60,96 cm. Les unités implicites DL, DP, DT, DA, et DE sont universelles et n’ont pas de traduction.
  
## <a name="default-units-of-measure"></a>Unités de mesure par défaut

Le tableau ci-dessous présente les unités de mesure par défaut avec les paramètres correspondants dans l’interface utilisateur.
  
|**Unité de mesure par défaut**|**Équivalent dans l’interface utilisateur**|
|:-----|:-----|
|**visDrawingUnits** <br/> |Unités de la cellule DrawingScale de la page ou de la forme de base contenant la cellule.  <br/> |
|**visPageUnits** <br/> |Unités sélectionnées dans la zone **unités de mesure** sous l’onglet **Propriétés de Page** de la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ).  <br/> |
|**visTypeUnits** <br/> |Unités sélectionnées dans la zone de **texte** sous **Afficher** sous l’onglet **Avancé** de la boîte de dialogue **Options Visio** (cliquez sur l’onglet **fichier** , puis cliquez sur **Options**).  <br/> |
|**visAngleUnits** <br/> |Unités sélectionnées dans la zone **Angle** section **affichage** sous l’onglet **Avancé** de la boîte de dialogue **Options Visio** .  <br/> |
|**visDurationUnits** <br/> |Unités sélectionnées dans la zone **durée** sous **Afficher** sous l’onglet **Avancé** de la boîte de dialogue **Options Visio** .  <br/> |
   

