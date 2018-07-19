---
title: Formats numériques personnalisés pour la fonction Format (application web personnalisée Access)
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 97efe972-d873-47d7-be81-8ae3461870c4
description: Découvrez comment contrôler l’affichage d’un nombre en créant un format numérique défini par l’utilisateur.
ms.openlocfilehash: fac128ce13edf89105fbee7319533e1a3f346d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781847"
---
# <a name="custom-numeric-formats-for-the-format-function-access-custom-web-app"></a>Formats numériques personnalisés pour la fonction Format (application web personnalisée Access)

Découvrez comment contrôler l’affichage d’un nombre en créant un format numérique défini par l’utilisateur.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-FR/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 

Vous pouvez modifier l'affichage d'un nombre en créant un format numérique défini par l'utilisateur. Un format numérique défini par l'utilisateur peut comporter entre une et trois sections séparées par des points-virgules (;). Si l'argument Style de la fonction [Fonction de format (application web personnalisé de l'accès)](format-function-access-custom-web-app.md) contient l'un des formats numériques prédéfinis, une seule section est autorisée. 
  
## <a name="format-specifications"></a>Spécifications de format
<a name="bk_addresources"> </a>

Le tableau suivant présente les caractères que vous pouvez utiliser pour créer des formats numériques définis par l’utilisateur.
  
|**Spécification de format**|**Description**|
|:-----|:-----|
|Aucune  <br/> |Affiche le nombre sans mise en forme.  <br/> |
|**0** (caractère zéro)  <br/> |Espace réservé à un chiffre. Affichage d’un chiffre ou d’un zéro. Si l’expression contient un chiffre à la position occupée par le 0 dans la chaîne de mise en forme, le chiffre est affiché ; sinon un zéro est affiché à cet emplacement.  <br/> Si le nombre possède moins de chiffres que de zéros (de part et d’autre du séparateur décimal) dans l’expression de mise en forme, les zéros non significatifs et les zéros à droite sont affichés. Si le nombre compte plus de chiffres à droite du séparateur décimal que de zéros à droite de ce séparateur dans l’expression de mise en forme, le nombre est arrondi à autant de chiffres après la virgule qu’il y a de zéros. Si le nombre compte plus de chiffres à gauche du séparateur décimal qu’il y a de zéros à gauche de ce séparateur dans l’expression de mise en forme, les chiffres supplémentaires sont affichés sans modification.  <br/> |
|#  <br/> |Espace réservé à un chiffre. Affichage d’un chiffre ou d’aucun caractère. Si l’expression mise en forme contient un chiffre à la position occupée par le caractère # dans la chaîne de mise en forme, le chiffre est affiché ; sinon, rien n’est affiché à cet emplacement.  <br/> Ce symbole se comporte exactement comme l’espace réservé au chiffre 0. Cependant, les zéros non significatifs et les zéros à droite ne sont pas affichés si le nombre compte un nombre de chiffres inférieur au nombre de caractères # situés de part et d’autre du séparateur décimal dans l’expression de mise en forme.  <br/> |
|. (point)  <br/> |Espace réservé au séparateur décimal. L’espace réservé au séparateur décimal détermine le nombre de chiffres affichés de part et d’autre du séparateur décimal. Si l’expression de mise en forme contient uniquement des caractères # à gauche de ce symbole, les nombres inférieurs à 1 commencent par ce séparateur. Pour afficher les nombres fractionnaires avec un zéro non significatif, indiquez un zéro comme premier espace réservé à gauche du séparateur décimal. Dans certains paramètres régionaux, le séparateur décimal est représenté par une virgule. Le caractère réservé au séparateur décimal dans la sortie mise en forme dépend du format des nombres utilisé par le système. Par conséquent, vous devez utiliser un point en tant qu’espace réservé au séparateur décimal dans les formats, même si vos paramètres régionaux utilisent la virgule comme séparateur décimal. La chaîne de mise en forme apparaît dans le format correct selon les paramètres régionaux.  <br/> |
|%  <br/> |Espace réservé au signe pourcentage. L’expression est multipliée par 100. Le signe pourcentage (%) est inséré à la position où il apparaît dans la chaîne de mise en forme.  <br/> |
|, (virgule)  <br/> |Séparateur de milliers. Le séparateur de milliers sépare les milliers des centaines dans un nombre qui comporte au moins quatre chiffres à gauche du séparateur décimal. Le séparateur de milliers standard est utilisé si le format contient un séparateur de milliers entouré d’espaces réservés à un chiffre (0 ou #).  <br/> Un séparateur de milliers placé immédiatement à gauche du séparateur décimal (si une décimale est précisée) ou placé le plus à droite possible dans la chaîne signifie « reformuler le nombre en le divisant par 1 000, en arrondissant si nécessaire ». Les nombres compris entre 500 et 1 000 sont affichés comme 1, et les nombres inférieurs à 500 sont affichés comme 0. Deux séparateurs de milliers adjacents à cet emplacement effectue une mise à l’échelle par un facteur de 1 million et un facteur supplémentaire de 1 000 pour chaque séparateur supplémentaire.  <br/> Les séparateurs multiples se trouvant ailleurs qu’immédiatement à gauche du séparateur décimal ou le plus à droite possible dans la chaîne sont traités uniquement en tant que spécification de l’utilisation d’un séparateur de milliers. Dans certains paramètres régionaux, un point est utilisé comme séparateur de milliers. Le caractère effectivement utilisé comme séparateur de milliers dans la sortie mise en forme dépend du format numérique reconnu par le système. Par conséquent, vous devez utiliser la virgule comme séparateur de milliers dans vos mises en forme, même si d’après vos paramètres régionaux, le point est utilisé comme séparateur de milliers. La chaîne mise en forme s’affiche dans le format correct pour les paramètres régionaux.  <br/> Voici, par exemple, trois chaînes de format :  <br/> « #,0. », utilise le séparateur de milliers pour mettre en forme le nombre 100 millions comme « 100,000,000 ».  <br/> « #0,. », utilise la mise à l’échelle par un facteur de mille pour mettre en forme le nombre 100 millions comme « 100000 ».  <br/> « #,0,. », utilise le séparateur de milliers et la mise à l’échelle par un facteur de mille pour mettre en forme le nombre 100 millions comme « 100,000 ».  <br/> |
|: (deux-points)  <br/> |Séparateur horaire. Dans certains paramètres régionaux, le séparateur horaire est représenté par d’autres caractères. Le séparateur horaire dissocie les heures, les minutes et les secondes lorsque des valeurs horaires sont mises en forme. Le caractère effectivement utilisé comme séparateur horaire dans la sortie mise en forme dépend des paramètres du système.  <br/> |
|/ (barre oblique)  <br/> |Séparateur de date. Dans certains paramètres régionaux, le séparateur de date est représenté par d’autres caractères. Le séparateur de date dissocie le jour, le mois et l’année lorsque des valeurs de date sont mises en forme. Le caractère effectivement utilisé comme séparateur de date dans la sortie mise en forme dépend des paramètres du système.  <br/> |
|**E- , E+ , e- , e+** <br/> |Format scientifique. Si l’expression de mise en forme contient au moins un espace réservé à un chiffre (0 ou #) à droite de E-, E+, e- ou e+, le nombre est affiché au format scientifique, et E ou e est inséré entre le nombre et son exposant. Le nombre d’espaces réservés à un chiffre sur la gauche détermine le nombre de chiffres de l’exposant. Utilisez E- ou e- pour placer un signe moins devant des exposants négatifs. Utilisez E+ ou e+ pour placer un signe moins devant des exposants négatifs et un signe plus devant des exposants positifs. Vous devez également inclure des espaces réservés à des chiffres à droite de ce symbole pour obtenir une mise en forme adéquate.  <br/> |
|**- + $ ( )** <br/> |Caractères littéraux. Ces caractères sont affichés exactement tels que vous les avez saisis dans la chaîne de mise en forme. Pour afficher un autre caractère que ceux répertoriés, faites-le précéder d'une barre oblique inversée (\) ou placez-le entre guillemets (« »).  <br/> |
|\ (barre oblique inversée)  <br/> |Affichage du caractère suivant de la chaîne de mise en forme. Pour afficher un caractère doté d'une signification spéciale sous la forme de caractère littéral, faites-le précéder d'une barre oblique inverse (\). La barre oblique inverse n'est pas affichée. Son utilisation revient à placer entre guillemets doubles le caractère suivant. Pour afficher une barre oblique inverse, utilisez deux barres obliques inverses (\\).  <br/> Les caractères de mise en forme de date et heure (a, c, d, h, m, n, p, q, s, t, w, y, / et :), les caractères de mise en forme numérique (#, 0, %, E, e, séparateur décimal et séparateur des milliers) et les caractères de mise en forme de chaîne (@, &amp;, \<, \> et !) sont des exemples de caractères qui ne peuvent pas être affichés comme caractères littéraux.  <br/> |
|"ABC"  <br/> |Affichage de la chaîne entre guillemets doubles (" "). Pour inclure une chaîne dans l’argument Style dans du code, vous devez utiliser la fonction Chr(34) pour placer le texte entre guillemets doubles (34 est le code de caractère correspondant aux guillemets doubles (")).  <br/> |
   
Le tableau suivant contient des exemples d’expressions de mise en forme pour les nombres. (Tous ces exemples supposent que les paramètres régionaux de votre système sont English-US). La première colonne contient les chaînes de mise en forme pour la fonction Format. Les autres colonnes contiennent le résultat obtenu si les données mises en forme ont la valeur donnée dans les en-têtes de colonne.
  
|**Format (Style)**|**« 5 » au format**|**« -5 » au format**|**« 0,5 » au format**|**« 0 » au format**|
|:-----|:-----|:-----|:-----|:-----|
|Une chaîne de longueur nulle ("").  <br/> |5  <br/> |-5  <br/> |0.5  <br/> |0  <br/> |
|0  <br/> |5  <br/> |-5  <br/> |1  <br/> |0  <br/> |
|0.00  <br/> |5.00  <br/> |-5.00  <br/> |0.50  <br/> |0.00  <br/> |
|#,##0  <br/> |5  <br/> |-5  <br/> |1  <br/> |0  <br/> |
|$#,##0;($#,##0)  <br/> |$5  <br/> |($5)  <br/> |$1  <br/> |$0  <br/> |
|$#,##0.00;($#,##0.00)  <br/> |$5.00  <br/> |($5.00)  <br/> |$0.50  <br/> |$0.00  <br/> |
|0%  <br/> |500%  <br/> |-500%  <br/> |50%  <br/> |0%  <br/> |
|0.00%  <br/> |500.00%  <br/> |-500.00%  <br/> |50.00%  <br/> |0.00%  <br/> |
|0.00E+00  <br/> |5.00E+00  <br/> |-5.00E+00  <br/> |5.00E-01  <br/> |0.00E+00  <br/> |
|0.00E-00  <br/> |5.00E00  <br/> |-5.00E00  <br/> |5.00E-01  <br/> |0.00E00  <br/> |
|"$#,##0;;\Z\e\r\o"  <br/> |$5  <br/> |$-5  <br/> |$1  <br/> |Zero  <br/> |
   
## <a name="remarks"></a>Remarques
<a name="bk_addresources"> </a>

Si deux points-virgules se suivent immédiatement, la section manquante est affichée selon le format de la valeur positive.
  
## <a name="see-also"></a>Voir aussi

- [Fonction de format (application web personnalisée Access)](format-function-access-custom-web-app.md) 
- [Formats de date et d'heure personnalisés pour la fonction Format (application web personnalisée Access)](custom-date-and-time-formats-for-the-format-function-access-custom-web-app.md)
  

