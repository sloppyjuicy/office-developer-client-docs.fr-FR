---
title: À propos des modèles de format
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251831
localization_priority: Normal
ms.assetid: df4c1c70-8b41-c046-7415-643188af0e06
description: Un modèle de format sert à déterminer l’affichage d’une valeur. Par exemple, vous pouvez contrôler le nombre de chiffres à droite ou à gauche de la virgule décimale ou l’affichage d’une chaîne de texte en majuscules ou minuscules.
ms.openlocfilehash: 7043c9819f41ec2c08345c84010328be75677918
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344554"
---
# <a name="about-format-pictures"></a>À propos des modèles de format

Un modèle de format sert à déterminer l’affichage d’une valeur. Par exemple, vous pouvez contrôler le nombre de chiffres à droite ou à gauche de la virgule décimale ou l’affichage d’une chaîne de texte en majuscules ou minuscules.
  
> [!NOTE]
> Pour définir un modèle de format de date ou d’heure à l’aide de la mise en forme du système Microsoft Office, placez le modèle de format entre deux accolades, par exemple, « {{j/m/aa}} ». Si vous utilisez un format prédéfini, par exemple, 201, mettez-le entre accolades et chevrons, comme suit: «{\<201\>}» 
  
Les sections suivantes montrent les symboles que vous pouvez utiliser pour mettre en forme différents types de valeurs pour l'affichage.
  
## <a name="string-and-numeric-values"></a>Chaînes et valeurs numériques

|**Caractère**|**Description**|
|:-----|:-----|
|#  <br/> |Emplacement réservé à un chiffre. Affiche un chiffre ou rien. Les zéros placés en début et en fin ne s’affichent pas. Si le nombre de chiffres est supérieur à l’espace qui leur est réservé à gauche du séparateur décimal, tous les chiffres s’affichent. En revanche, si le nombre de chiffres est supérieur à l’espace qui leur est réservé à droite du séparateur décimal, la fraction est arrondie au nombre d’emplacements. Dans le cas d’une cote, si l’emplacement réservé correspond au chiffre le plus à gauche, les sous-unités égales à 0 ne s’affichent pas.  <br/> Par exemple, FORMAT(0 cm 30 mm,"#,##u") affiche 30 mm.  <br/> |
|0  <br/> |Emplacement réservé à un chiffre (zéro). Affiche un chiffre ou rien. Les zéros placés en début et en fin s’affichent. Si le nombre de chiffres est supérieur à l’espace qui leur est réservé à gauche du séparateur décimal, tous les chiffres s’affichent. En revanche, si le nombre de chiffres est supérieur à l’espace qui leur est réservé à droite du séparateur décimal, la fraction est arrondie au nombre d’emplacements. Dans le cas d’une cote, les sous-unités égales à 0 s’affichent.  <br/> Par exemple, FORMAT(2 cm 11,33 mm,",## u") affiche 2 cm 11,33 mm.  <br/> |
|.  <br/> |Emplacement réservé au séparateur décimal. Détermine le nombre de chiffres à gauche et à droite du séparateur décimal. Dans une unité composée de plusieurs parties, le séparateur décimal est utilisé dans la sous-unité la plus petite (la plus à droite). Affiche le caractère décimal défini dans les paramètres **Région et langue** du système (Panneau de configuration).<br/> Par exemple, FORMAT(250 cm;"0,000 u") affiche 250,000 cm.  <br/> |
|,  <br/> |Séparateur des milliers. S’il est entouré d’emplacements réservés à des chiffres (# ou 0), le séparateur permet de dissocier les milliers des centaines dans un nombre qui comporte au moins quatre chiffres à gauche du séparateur décimal. Affiche le séparateur des milliers défini dans les paramètres **Région et langue** du système (Panneau de configuration).<br/> |
|E- E+ e- e+  <br/> |Format scientifique. Si le format contient au moins un emplacement réservé à un chiffre à droite de ces symboles, le nombre s’affiche au format scientifique. Insère le E ou le e entre le nombre et son exposant. Dans le cas de E+ ou e+, affiche le signe + avant les exposants positifs et le signe - avant les exposants négatifs. Dans le cas de E- ou e-, n’affiche le signe - que lorsque l’exposant est négatif.  <br/> Par exemple FORMAT(12345,67;"###,#e+#") affiche 0,123,5e+2.  <br/> |
|u ou U  <br/> |Emplacement réservé à un intitulé court. Insère des étiquettes d'unité abrégées après chaque sous-unité. Par exemple: in., ft., deg. L'espace réservé U insère des étiquettes à casse mixte, tandis que l'espace réservé u insère des étiquettes en minuscules. Insère le même nombre d’espaces avant l’intitulé et avant l’emplacement.  <br/> Par exemple, FORMAT(12 c 13 d;"#u") affiche 13c1.  <br/> |
|uu ou UU  <br/> |Emplacement réservé aux intitulés longs. Insère des intitulés après chaque sous-unité. Par exemple: pouces, pieds, degrés l'espace réservé U insère des étiquettes à casse mixte, tandis que l'espace réservé u insère des étiquettes en minuscules. Insère le même nombre d’espaces avant l’intitulé et avant l’emplacement réservé.  <br/> Par exemple, FORMAT(12,43 cm;"# #/4 UU") affiche 12 2/4 CENTIMETRES.  <br/> |
|uuu ou UUU  <br/> |Emplacement réservé à un intitulé universel. Insère le symbole universel (propre à l’application Microsoft Visio) des intitulés d’unité après chaque sous-unité. L'espace réservé U insère des étiquettes à casse mixte, tandis que l'espace réservé u insère des étiquettes en minuscules. Insère le même nombre d’espaces avant l’intitulé et avant l’emplacement.  <br/> |
|/  <br/> |Emplacement réservé à la fraction. Affiche l’expression sous la forme d’un entier avec fraction si un emplacement réservé à un chiffre se trouve en début de chaîne. Dans le cas contraire, seul le nombre du numérateur s’affiche. Si un nombre suit l’emplacement réservé du chiffre dans le dénominateur, arrondit la fraction à la fraction la plus proche dont le numérateur est 1 et la simplifie. Si un nombre est défini dans le dénominateur sans emplacement réservé au chiffre, arrondit à la fraction la plus proche sans la simplifier.  <br/> Par exemple, FORMAT(12,43;"# #/4") affiche 12 2/4.  <br/> |
|espace  <br/> |Affiche un espace. Pour afficher un autre caractère, utilisez la barre\) oblique inverse (caractère.  <br/> |
   
## <a name="currency-values"></a>Valeurs monétaires

|**Caractère**|**Description**|
|:-----|:-----|
|$  <br/> |Symbole monétaire. Affiche le symbole monétaire défini dans les paramètres **Région et langue** du système (Panneau de configuration).  <br/> |
|u ou U  <br/> |Emplacement réservé à un intitulé court. Insère le symbole standard associé à une monnaie locale ou la constante à trois caractères correspondant aux monnaies étrangères. Par exemple, 99,00 €; 42,70 USD. L'espace réservé u insère des minuscules et U les étiquettes de casse mixte.  <br/> |
|uu ou UU  <br/> |Emplacement réservé aux intitulés longs. Insère des intitulés correspondant aux unités monétaires au format complet après chaque sous-unité. Par exemple : Dollar US, euro. L'espace réservé u insère des minuscules et U les étiquettes de casse mixte.  <br/> |
|uuu ou UUU  <br/> |Emplacement réservé à un intitulé universel. Insère la constante à trois chiffres universelle ou toutes les unités monétaires après chaque sous-unité. Par exemple, 99,00 €; 42,70 USD. L'espace réservé u insère des minuscules et U les étiquettes de casse mixte. Insère le même nombre d’espaces avant l’intitulé et avant l’emplacement.  <br/> |
   
## <a name="text-values"></a>Valeurs de texte

|**Caractère**|**Description**|
|:-----|:-----|
|\  <br/> |Affiche le caractère suivant tel quel. Pour afficher le caractère barre oblique inverse \\, tapez. Voir aussi « texte ».  <br/> |
|"texte" ou ’texte’  <br/> |Affiche le texte entre guillemets tel quel. Voir aussi \ (barre oblique inverse).  <br/> |
|@  <br/> |Emplacement réservé à du texte. Remplace une chaîne si la valeur de l’expression est une chaîne.  <br/> Par exemple, FORMAT("Bonjour", "’Vous avez entré (’@’)’" ) produit « Vous avez entré (Bonjour) ».  <br/> |
|@+  <br/> |Emplacement réservé à du texte en majuscules. Pour les valeurs de chaîne, remplace l’entrée par des majuscules.  <br/> Par exemple, FORMAT("Bonjour", "@ @+ @-" ) produit « Bonjour BONJOUR bonjour) ».  <br/> |
|@-  <br/> |Emplacement réservé à du texte. Pour les valeurs de chaîne, remplace l’entrée par des minuscules.  <br/> Par exemple, FORMAT("Bonjour", "@ @+ @-" ) produit « Bonjour BONJOUR bonjour) ».  <br/> |
   
## <a name="date-values"></a>Valeurs de date

|**Caractère**|**Description**|
|:-----|:-----|
|c ou C  <br/> |Emplacement réservé à une date ou à une heure. Affiche les valeurs de date et d’heure à l’aide du format abrégé (c) ou complet (C) et du format horaire standard. Les versions de Visio 4.0 et supérieures ignorent cet emplacement réservé.  <br/> Par exemple : FORMAT(DATETIME("6/25/07 12:05"),"C") affiche Lundi 25 juin 2007 12:05:00 PM. FORMAT(DATETIME("25 juin 2007"),"c") affiche 25/06/2007.  <br/> |
|/  <br/> |Séparateur de date. Si l’expression est une date, sépare les composants de date. Affiche le séparateur de date défini dans les paramètres **Région et langue** du système (Panneau de configuration).<br/> |
| [ ]  <br/> |Emplacement réservé à une durée écoulée. Utilisée avec les emplacements réservés j, jj, s et ss pour afficher les unités de durée.  <br/> Par exemple, [j] ou [jj] représente les jours écoulés et [s] ou [ss] les semaines écoulées.  <br/> |
|d  <br/> |Emplacement réservé au jour. Affiche le jour sous forme de nombre (1-31) sans ajouter de zéro en début de chaîne.  <br/> |
|dd  <br/> | Emplacement réservé au jour. Affiche le jour sous forme de nombre (01-31) avec un zéro en début de chaîne.  <br/> |
|jjj ou s  <br/> |Emplacement réservé au jour de la semaine au format abrégé. Affiche le jour sous forme d’abréviation (Lun-Dim).  <br/> |
|dddd ou w  <br/> |Emplacement réservé au jour de la semaine au format complet. Affiche le nom complet du jour (Lundi-Dimanche).  <br/> |
|ddddd  <br/> |Emplacement réservé à une date courte. Affiche une date sous la forme courte définie dans les paramètres **Région et langue** du système (Panneau de configuration).<br/> |
|dddd  <br/> |Emplacement réservé à une date longue. Affiche une date sous la forme longue définie dans les paramètres **Région et langue** du système (Panneau de configuration).  <br/> |
|D  <br/> |Emplacement réservé à la date pour le chinois traditionnel. Affiche le jour du mois sous forme de représentation textuelle du nombre ordinal. Spécifique aux paramètres régionaux.  <br/> |
|D_c  <br/> |Emplacement réservé à la date pour le chinois traditionnel. Affiche le jour du mois sous forme de représentation textuelle du nombre ordinal. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|w_c ou w_c  <br/> |Emplacement réservé à la date pour le chinois traditionnel. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|w_e  <br/> |Emplacement réservé au jour de la semaine au format abrégé pour l’anglais. Affiche le jour sous forme d’abréviation (Sun-Sat). Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|w_j  <br/> |Emplacement réservé au jour de la semaine au format complet pour le japonais. Affiche le nom complet du jour. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|w_k  <br/> |Emplacement réservé au jour de la semaine au format complet pour le coréen. Affiche le nom complet du jour. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|w_s ou w_s  <br/> |Emplacement réservé au jour de la semaine pour le chinois simplifié. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|ww_e  <br/> |Emplacement réservé au jour de la semaine au format complet pour l’anglais. Affiche le nom complet du jour (Sunday-Saturday). Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|ww_j  <br/> |Emplacement réservé au jour de la semaine au format complet pour le japonais. Affiche le nom complet du jour. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|w_k  <br/> |Emplacement réservé au jour de la semaine au format complet pour le coréen. Affiche le nom complet du jour. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|M  <br/> |Emplacement réservé au mois. Affiche le mois sous forme de nombre (1-12) sans ajouter de zéro en début de chaîne. Voir aussi m (emplacement réservé aux minutes).  <br/> |
|MM  <br/> |Emplacement réservé au mois. Affiche le mois sous forme de nombre (01-12) avec un zéro en début de chaîne. Voir aussi m (emplacement réservé aux minutes).  <br/> |
|MMM  <br/> |Emplacement réservé au mois. Affiche le mois au format abrégé (Jan-Déc).  <br/> |
|MMMM  <br/> |Emplacement réservé au mois. Affiche le nom complet du mois (Janvier-Décembre).  <br/> |
|MMMM_c  <br/> |Emplacement réservé à la date pour le chinois traditionnel. Affiche le nom complet du mois. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|MMMM_e  <br/> |Emplacement réservé à la date pour l’anglais. Affiche le nom complet du mois. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|yy  <br/> |Emplacement réservé à l’année. Affiche l’année sous forme de nombre à deux chiffres (00-99).  <br/> |
|yyyy  <br/> |Emplacement réservé à l’année. Affiche l’année sous forme de nombre à quatre chiffres (1900-2078).  <br/> |
|g  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le japonais, affiche la version abrégée de l’ère Gengo. Pour le coréen, affiche l’intitulé de l’année coréenne suivi d’un espace.  <br/> |
|g_j  <br/> |Emplacement réservé à l’année. Pour le japonais, affiche la version abrégée de l’ère Gengo. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|gg ou G  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le chinois traditionnel, affiche la version de l’intitulé traditionnel de l’année. Pour le japonais, affiche la version abrégée de l’ère Gengo en Kanji. Pour le coréen, affiche l’intitulé de l’année coréenne suivi d’un espace.  <br/> |
|gg_c  <br/> |Emplacement réservé à l’année. Pour le chinois traditionnel, affiche la version abrégée de l’intitulé traditionnel de l’année. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|gg_j  <br/> |Emplacement réservé à l’année. Pour le japonais, affiche la version abrégée de l’ère Gengo en Kanji. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|gg_k  <br/> |Emplacement réservé à l’année. Pour le coréen, affiche l’intitulé de l’année coréenne suivi d’un espace. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|ggg ou GG  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le chinois traditionnel, affiche la version complète de l’intitulé traditionnel de l’année. Pour le japonais, affiche la version complète de l’ère Gengo en Kanji. Pour le coréen, affiche l’intitulé de l’année coréenne suivi d’un espace.  <br/> |
|ggg_c  <br/> |Emplacement réservé à l’année. Pour le chinois traditionnel, affiche la version complète de l’intitulé traditionnel de l’année. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|ggg_j  <br/> |Emplacement réservé à l’année. Pour le japonais, affiche la version complète de l’ère Gengo en Kanji. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|éditeur  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le chinois traditionnel, affiche une chaîne représentant l’année julienne. Pour le japonais, affiche l’année Gengo sous forme d’un ou deux chiffres, sans zéro en début de chaîne. Pour le coréen, affiche l’année coréenne sous forme d’un nombre arabe à quatre chiffres.  <br/> |
|e_c  <br/> |Emplacement réservé à l’année. Pour le chinois traditionnel, affiche une chaîne représentant l’année julienne. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|e_j  <br/> |Emplacement réservé à l’année. Pour le japonais, affiche l’année Gengo sous forme d’un nombre arabe à un ou deux chiffres. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|e_k  <br/> |Emplacement réservé à l’année. Pour le coréen, affiche l’année coréenne sous forme d’un nombre arabe à quatre chiffres. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|E  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le chinois, affiche une chaîne représentant l’année de la République. Pour le japonais, affiche l’année Gengo sous forme d’un ou deux chiffres, sans zéro en début de chaîne. Pour le coréen, affiche l’année coréenne sous forme d’un nombre arabe à quatre chiffres.  <br/> |
|E_c  <br/> |Emplacement réservé à l’année. Pour le chinois traditionnel, affiche une chaîne représentant l’année de la République. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|EE  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le chinois, affiche une chaîne représentant l’année julienne. Pour le japonais, affiche l’année Gengo sous forme d’un nombre arabe à deux chiffres avec un zéro en début de chaîne, si nécessaire. Pour le coréen, affiche l’année coréenne sous forme d’un nombre arabe à quatre chiffres.  <br/> |
|ee_j  <br/> |Emplacement réservé à l’année. Pour le japonais, affiche l’année Gengo sous forme d’un nombre arabe à deux chiffres. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|EE  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le chinois traditionnel, affiche une chaîne représentant l’année de la République. Pour le japonais, affiche l’année Gengo sous forme d’un nombre arabe à deux chiffres avec un zéro en début de chaîne, si nécessaire. Pour le coréen, affiche l’année coréenne sous forme d’un nombre arabe à quatre chiffres.  <br/> |
|n ou N  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le chinois, affiche l’année de la République sous forme d’un nombre arabe. Pour le japonais, affiche l’année Gengo sous forme d’un ou deux chiffres, sans zéro en début de chaîne. Pour le coréen, affiche l’année coréenne sous forme d’un nombre arabe à quatre chiffres.  <br/> |
|n_c  <br/> |Emplacement réservé à l’année. Pour le chinois, affiche l’année de la République sous forme d’un nombre arabe. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|nn ou NN  <br/> |Emplacement réservé à l’année. Spécifique aux paramètres régionaux. Pour le chinois traditionnel, affiche l’année de la République sous forme d’un nombre arabe. Pour le japonais, affiche l’année Gengo sous forme d’un nombre arabe à deux chiffres avec un zéro en début de chaîne, si nécessaire. Pour le coréen, affiche l’année coréenne sous forme d’un nombre arabe à quatre chiffres.  <br/> |
   
## <a name="time-values"></a>Valeurs d’heure

|**Caractère**|**Description**|
|:-----|:-----|
|:  <br/> |Séparateur horaire. Affiche l’heure définie dans les paramètres **Région et langue** du système (Panneau de configuration).<br/> |
|[ ]  <br/> |Emplacement réservé au temps écoulé. Utilisé avec les emplacements h, hh, m, mm, s et ss pour afficher les unités de durée. Par exemple, [h] ou [hh] représente les heures écoulées, [m] ou [mm] les minutes écoulées et [s] ou [ss] les secondes écoulées.  <br/> |
|h  <br/> |Emplacement réservé à l’affichage des heures. Affiche l’heure au format 12 heures sans zéro en début de chaîne (0-12).  <br/> |
|hh  <br/> |Emplacement réservé à l’affichage des heures. Affiche l’heure au format 12 heures avec un zéro en début de chaîne (00-12).  <br/> |
|H  <br/> |Emplacement réservé à l’affichage des heures. Affiche l’heure au format 24 heures sans zéro en début de chaîne (0-24).  <br/> |
|HH  <br/> |Emplacement réservé à l’affichage des heures. Affiche l’heure au format 24 heures avec un zéro en début de chaîne (00-24).  <br/> |
|m  <br/> |Emplacement réservé à l’affichage des minutes. Affiche les minutes sans zéro en début de chaîne (0-59).  <br/> |
|mm  <br/> |Emplacement réservé à l’affichage des minutes. Affiche les minutes avec un zéro en début de chaîne (00-59).  <br/> |
|s  <br/> |Emplacement réservé à l’affichage des secondes. Affiche les secondes sans zéro en début de chaîne (0-59).  <br/> |
|ss  <br/> |Emplacement réservé à l’affichage des secondes. Affiche les secondes avec un zéro en début de chaîne (00-59).  <br/> |
|t  <br/> |Abréviation matin/après-midi. Affiche l’abréviation définie dans les paramètres **Région et langue** du système (Panneau de configuration).<br/> |
|tt  <br/> |Indicateur matin/après-midi. Affiche l’indicateur complet défini dans les paramètres **Région et langue** du système (Panneau de configuration).<br/> |
|t_c ou tt_c  <br/> |Indicateur matin/après-midi en chinois traditionnel. Affiche l’indicateur. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|t_k ou tt_k  <br/> |Indicateur matin/après-midi en coréen. Affiche l’indicateur. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|t_j ou tt_j  <br/> |Indicateur matin/après-midi en japonais. Affiche l’indicateur. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|t_e  <br/> |Indicateur matin/après-midi en anglais. Affiche l’indicateur abrégé. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|tt_e  <br/> |Indicateur matin/après-midi en anglais. Affiche l’indicateur complet. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|t_s ou tt_s  <br/> |Indicateur matin/après-midi en chinois simplifié. Affiche l’indicateur. Indépendant des paramètres régionaux de l’utilisateur.  <br/> |
|T  <br/> |Format horaire standard.  <br/> |
   

