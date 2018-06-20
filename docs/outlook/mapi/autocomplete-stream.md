---
title: Flux de saisie semi-automatique
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782977"
---
# <a name="autocomplete-stream"></a>Flux de saisie semi-automatique

  
  
**S’applique à**: Outlook 
  
En plus de savoir comment Microsoft Outlook interagit avec le flux de saisie semi-automatique, vous devez également comprendre le format binaire de l’objet stream de saisie semi-automatique.
  
Le flux de saisie semi-automatique est un ensemble de lignes de propriété de destinataire qui sont enregistrés sous la forme d’un flux binaire avec des métadonnées de référence qui sont utilisé uniquement par Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 et Microsoft Outlook 2003. Les métadonnées sont pertinentes pour les interactions d’Outlook avec le flux de saisie semi-automatique afin que les tierces parties doit conserver Nouveautés dans chaque bloc de métadonnées lorsqu’ils enregistrent un flux de saisie semi-automatique modifié. En d’autres termes, les tierces parties doit modifier uniquement la partie de l’ensemble de lignes du format binaire et de conserver ce qui a déjà été dans les blocs de métadonnées de l’objet stream de saisie semi-automatique.
  
## <a name="stream-visualization"></a>Visualisation du flux de données

La disposition de haut niveau de l’objet stream de saisie semi-automatique est la suivante :
  
Métadonnées (4 octets)
  
Numéro de Version principale (4 octets)
  
Numéro de Version secondaire (4 octets)
  
Nombre de lignes n (4 octets)
  
Nombre de propriétés p dans la ligne 1 (4 octets)
  
Balise de propriété propriété 1 (4 octets)
  
Propriété 1 du réservée données (4 octets)
  
Union de valeur de propriété 1 (8 octets)
  
Données de valeur de propriété 1 (0 ou variables octets)
  
… (propriété 2 par le biais de la propriété P-1)
  
Balise de propriété de la propriété du p (4 octets)
  
Propriété p de réservé à des données (4 octets)
  
Union de valeur de propriété de p (8 octets)
  
Données de la propriété de p la valeur (0 ou variables octets)
  
Nombre de propriétés q de la deuxième ligne (4 octets)
  
… (deux propriétés de ligne)
  
… (ligne 3 à n-1 de la ligne)
  
Nombre de propriétés r ligne n (4 octets)
  
… (ligne n's propriétés)
  
Nombre d’octets des informations supplémentaires eu (4 octets)
  
Informations supplémentaires (octets eu)
  
Métadonnées (8 octets)
  
Pour obtenir un exemple d’une structure binaire, voir exemple binaires dans les [Format de fichier NK2 Outlook 2003/2007 et des instructions pour les développeurs.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
  
## <a name="high-level-layout"></a>Disposition de haut niveau

D’une manière générale, la mise en page de l’objet stream de saisie semi-automatique est la suivante :
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Métadonnées  <br/> |4  <br/> |
|Numéro de Version majeure  <br/> |4  <br/> |
|Numéro de Version secondaire  <br/> |4  <br/> |
|Ensemble de lignes  <br/> |Variable  <br/> |
|Nombre d’octets des informations supplémentaires eu  <br/> |4  <br/> |
|Informations supplémentaires  <br/> |EU  <br/> |
|Métadonnées  <br/> |8  <br/> |
   
Lors de la lecture de ce flux, si la version principale est différente de 12, puis ce flux ne doit pas être lu ou écrit. La version secondaire actuelle du flux de saisie semi-automatique est 0, ce qui a la valeur 0 le nombre d’octets d’informations supplémentaires. Si la version secondaire est différente de 0, puis il y aura plus d’informations dans les informations supplémentaires qui doivent être lu lors de la lecture du flux et conservées lors de l’écriture du flux. La version secondaire vous devrez également être conservées lors de l’écriture de l’objet stream. Si ces deux éléments ne sont pas conservées, les instances d’Outlook qui écrit les informations supplémentaires perdre des données. 
  
> [!NOTE]
> Les applications ne doivent pas ajouter des données personnalisées dans le champ informations supplémentaires ou de modifier la version secondaire que cette fonctionnalité est pour prendre en charge des extensions Outlook vers le format et tiers arbitraires. 
  
## <a name="row-set-layout"></a>Disposition de l’ensemble de lignes

La disposition de l’ensemble de lignes est la suivante : 
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de lignes  <br/> |4  <br/> |
|Objet Rows  <br/> |Variable  <br/> |
   
Le nombre de lignes identifie le nombre de lignes fournis dans la partie suivante de la séquence de flux binaire.
  
## <a name="row-layout"></a>Mise en ligne

Chaque ligne est au format suivant :
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de propriétés  <br/> |4  <br/> |
|Propriétés  <br/> |Variable  <br/> |
   
Le nombre de propriétés identifie le nombre de propriétés fournis dans la partie suivante de la séquence de flux binaire.
  
## <a name="property-layout"></a>Propriété Layout

Chaque propriété est au format suivant :
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Balise de propriété  <br/> |4  <br/> |
|Données réservé  <br/> |4  <br/> |
|Propriété valeur Union  <br/> ||
|Données de la valeur  <br/> |0 ou variable (en fonction de la balise de propriétés)  <br/> |
   
## <a name="interpreting-the-property-value"></a>Interprétation de la valeur de propriété

L’Union de valeur de propriété et la valeur des données sont à être interprété en fonction de la balise de propriété dans les premières 4 octets du bloc de propriété. Cette balise de propriété est dans le même format qu’une balise de propriété MAPI. Bits 0 à 15 de la balise de propriété sont le type de propriété. Bits 16 à 31 sont l’identificateur de la propriété. Le type de propriété détermine la façon dont le reste de la propriété doit être lu.
  
## <a name="static-value"></a>Valeur statique

Certaines propriétés n’ont aucune donnée de valeur et contiennent uniquement des données dans l’union. Les types de propriété suivants (qui proviennent de la balise de propriété) doivent interpréter les données de propriété Union 8 octets comme suit :
  
|**Type de propriétés**|**Propriété interprétation Union**|
|:-----|:-----|
|PT_I2  <br/> |int court  <br/> |
|PT_LONG  <br/> |long  <br/> |
|PT_R4  <br/> |flottant  <br/> |
|PT_DOUBLE  <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |int court  <br/> |
|PT_SYSTIME  <br/> |FILETIME  <br/> |
|PT_I8  <br/> |LARGE_INTEGER  <br/> |
   
## <a name="dynamic-values"></a>Valeurs dynamiques

Autres propriétés disposent données dans un bloc de données de la valeur après que les premières 16 octets qui contiennent la balise de propriété, les données réservés et l’Union de valeur de propriété. Contrairement aux valeurs statiques, les données stockées dans l’union de la valeur de la propriété 8 octets sont sans effet sur la lecture. Lors de l’écriture, assurez-vous que vous remplissez ces 8 octets avec un élément. Toutefois, le contenu de 8 octets n’est pas important. Dans les valeurs dynamiques, type de la balise de propriété détermine comment interpréter les données de la valeur.
  
PT_STRING8 
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre d’octets n  <br/> |4  <br/> |
|Octets à être interprété comme une chaîne ANSI (y compris le terminateur NULL)  <br/> |n  <br/> |
   
PT_CLSID
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Octets à être interprété comme un GUID  <br/> |16  <br/> |
|||
   
PT_BINARY 
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre d’octets n  <br/> |4  <br/> |
|Octets à être interprété comme un tableau d’octets  <br/> |n  <br/> |
   
PT_ERROR
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre d’octets n  <br/> |4  <br/> |
|Octets à être interprété comme un tableau d’octets  <br/> |n  <br/> |
   
PT_MV_BINARY
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de tableaux binaires X  <br/> |4  <br/> |
|A exécuter d’octets contenant X tableaux binaires. Chaque tableau doit être interprété comme l’octet PT_BINARY exécuter.  <br/> |Variable  <br/> |
   
PT_MV_STRING8 (Outlook 2007, Outlook 2010 et Outlook 2013)
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de chaînes ANSI X  <br/> |4  <br/> |
|Une séquence d’octets qui contient les chaînes ANSI X. Chaque chaîne doit être interprété comme l’octet PT_STRING8 exécuter.  <br/> |Variable  <br/> |
   
PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de chaînes UNICODE X  <br/> |4  <br/> |
|Une séquence d’octets qui contient les chaînes X UNICODE. Chaque chaîne doit être interprété comme l’octet PT_UNICODE exécuter.  <br/> |Variable  <br/> |
   
## <a name="significant-properties"></a>Propriétés importantes

Comme mentionné précédemment dans cette rubrique, les blocs binaires qui représentent les propriétés ont des balises de propriété qui correspondent aux propriétés de destinataires de carnet d’adresses. Pour les propriétés qui ne sont pas répertoriées ici, vous pouvez consulter la description de la propriété à http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.
  
|**Nom de la propriété**|**Balise de propriété**|**Description (pour plus d’informations, voir MSDN)**|
|:-----|:-----|:-----|
|PR_NICK_NAME_W (ne pas transmis sur les destinataires, spécifiques aux flux de saisie semi-automatique uniquement)  <br/> |0x6001001f  <br/> |Cette propriété doit être la première dans chaque ligne du destinataire. Elle sert fonctionnellement un identificateur de clé pour la ligne du destinataire.  <br/> |
|PR_ENTRYID  <br/> |0x0FFF0102  <br/> |L’identificateur d’entrée adresse téléchargeable pour le destinataire.  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Nom d’affichage du destinataire.  <br/> |
|PR_EMAIL_ADDRESS_W  <br/> |0x3003001F  <br/> |Adresse de messagerie du destinataire (par exemple johndoe@contoso.com ou/o = Contoso/OU = Foo/cn = Recipients/cn = johndoe)  <br/> |
|PR_ADDRTYPE_W  <br/> |0x3002001F  <br/> |Type d’adresse du destinataire (par exemple, SMTP ou EX).  <br/> |
|CLÉ PR_SEARCH_KEY  <br/> |0x300B0102  <br/> |Clé de recherche MAPI du destinataire.  <br/> |
|PR_SMTP_ADDRESS_W  <br/> |0x39FE001f  <br/> |L’adresse du destinataire SMTP.  <br/> |
|PR_DROPDOWN_DISPLAY_NAME_W (ne pas transmis sur les destinataires, spécifiques aux flux de saisie semi-automatique uniquement)  <br/> |0X6003001f  <br/> |La chaîne d’affichage qui apparaît dans la liste de saisie semi-automatique.  <br/> |
|PR_NICK_NAME_WEIGHT (ne pas transmis sur les destinataires, spécifiques aux flux de saisie semi-automatique uniquement)  <br/> |0x60040003  <br/> |Le poids de cette entrée de saisie semi-automatique. Le poids est utilisé pour déterminer dans quel saisie semi-automatique ordre entrées se produisent lors de la recherche de la liste de saisie semi-automatique. Entrées avec plus d’importance affichera avant les entrées avec poids inférieur. La liste complète de saisie semi-automatique est triée par cette propriété. Le poids régulièrement diminue au fil du temps et augmente lorsque l’utilisateur envoie un message électronique à ce destinataire. Voir la description plus loin dans cette rubrique pour plus d’informations sur cette propriété.  <br/> |
   
PR_NICK_NAME_WEIGHT
  
Le jeu de lignes dans le flux de saisie semi-automatique est trié par ordre décroissant par la propriété PR_NICK_NAME_WEIGHT et le flux de saisie semi-automatique doit conserver toujours cette caractéristique triée. Par conséquent, toute modification apportée aux poids d’une ligne Assurez-vous également que position de la ligne conserve l’ordre de tri de l’ensemble de lignes. Les ajouts à l’ensemble de ligne doivent être insérés à la position correcte pour mettre à jour l’ordre de tri.
  
La valeur minimale de ce poids est 0 x 1 et la valeur maximale est LONG_MAX. Toutes les autres valeurs de l’épaisseur sont considérés comme non valides.
  
Lorsque Outlook 2007 envoie un message à ou résout un destinataire, elle augmentera poids de ce destinataire 0 x 2000.
  

