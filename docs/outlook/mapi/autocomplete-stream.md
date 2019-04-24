---
title: Flux de saisie semi-automatique
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8b5c5fee71db0fc7bdd6e01c58e9c9a9c3d9fa22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318080"
---
# <a name="autocomplete-stream"></a>Flux de saisie semi-automatique

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Outre le fait de savoir comment Microsoft Outlook interagit avec le flux de saisie semi-automatique, vous devez également comprendre le format binaire du flux de saisie semi-automatique.
  
Le flux de saisie semi-automatique est un ensemble de lignes de propriété de destinataire qui sont enregistrés sous la forme d’un flux binaire avec certaines métadonnées comptables, utilisées uniquement par Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 et Microsoft Outlook 2003. Les métadonnées sont pertinentes pour les interactions Outlook avec le flux de saisie semi-automatique afin que les tiers conservent ce qui se trouve dans chaque bloc de métadonnées lorsqu’ils enregistrent un flux de saisie semi-automatique modifié. En d’autres termes, les tiers doivent modifier uniquement la partie de ligne la plus riche du format binaire et conserver ce qui était déjà dans les blocs de métadonnées du flux de saisie semi-automatique.
  
## <a name="stream-visualization"></a>Visualisation de flux de données

La mise en page générale du flux de saisie semi-automatique est comme suit :
  
Métadonnées (4 octets)
  
Numéro de version majeure (4 octets)
  
Numéro de version mineure (4 octets)
  
Nombre n de lignes (4 octets)
  
Nombre de propriétés p dans la ligne une (4 octets)
  
Balise de propriété de la propriété 1 (4 octets)
  
Données réservées de la propriété 1 (4 octets)
  
Union de valeur de la propriété 1 (8 octets)
  
Données de valeur de la propriété 1 (0 octet ou octets variables)
  
… (propriété 2 via propriété P-1)
  
Balise de propriété de la propriété p (4 octets)
  
Données réservées de la propriété p (4 octets)
  
Union de valeur de la propriété p (8 octets)
  
Données de valeur de la propriété p (0 octet ou octets variables)
  
Nombre de propriétés q dans la ligne deux (4 octets)
  
… (propriétés de la ligne deux)
  
… (ligne 3 via ligne n-1)
  
Nombre de propriétés r dans la ligne n (4 octets)
  
… (propriétés de la ligne n)
  
Nombre d’octets des infos supplémentaires EI (4 octets)
  
Infos supplémentaires (octets EI)
  
Métadonnées (8 octets)
  
Pour un exemple de structure binaire, reportez-vous à la section Exemple binaire dans [Consignes pour le développement et le format de fichier NK2 Outlook 2003/2007](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
## <a name="high-level-layout"></a>Mise en page générale

De manière générale, la mise en page du flux de saisie semi-automatique est comme suit :
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Métadonnées  <br/> |4  <br/> |
|Numéro de version majeure  <br/> |4  <br/> |
|Numéro de version mineure  <br/> |4  <br/> |
|Ensemble de lignes  <br/> |Variable  <br/> |
|Nombre d’octets des infos supplémentaires EI  <br/> |4  <br/> |
|Informations supplémentaires  <br/> |EI   <br/> |
|Métadonnées  <br/> |8bits  <br/> |
   
Lors de la lecture de ce flux, si la version majeure n’est pas la 12, alors ce flux de données ne doit pas être lu ou écrit. La version mineure actuelle du flux de saisie semi-automatique est la 0, pour laquelle le nombre d’octets d’informations supplémentaire est égal à 0. Si la version mineure est différente de 0, il y aura alors des informations supplémentaires qui doivent être lues lors de la lecture du flux de données et conservées lors de la rédaction du flux d’informations. La version mineure doit également être conservée lors de la rédaction du flux de données. Si ces deux éléments ne sont pas conservés, les instances d’Outlook écrites par les informations supplémentaires perdent des données. 
  
> [!NOTE]
> Les applications ne doivent pas ajouter de données personnalisées au champ Informations supplémentaires ni changer la version mineure, car cette fonctionnalité doit prendre en charge les extensions Outlook au format et non des extensions tiers arbitraires. 
  
## <a name="row-set-layout"></a>Disposition de jeu de lignes

La disposition de jeu de lignes est comme suit : 
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de lignes  <br/> |4  <br/> |
|Lignes  <br/> |Variable  <br/> |
   
Le nombre de lignes identifie le nombre de lignes fournies dans la partie suivante de la séquence de flux binaire.
  
## <a name="row-layout"></a>Disposition de ligne

Chaque ligne correspond au format suivant :
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de propriétés  <br/> |4  <br/> |
|Propriétés  <br/> |Variable  <br/> |
   
Le nombre de lignes identifie le nombre de propriétés fournies dans la partie suivante de la séquence de flux binaire.
  
## <a name="property-layout"></a>Disposition de propriété

Chaque propriété correspond au format suivant :
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Balise de propriété  <br/> |4  <br/> |
|Données réservées  <br/> |4  <br/> |
|Union de valeur de la propriété  <br/> ||
|Données de la valeur  <br/> |0 ou variable (en fonction de la balise de proposition)  <br/> |
   
## <a name="interpreting-the-property-value"></a>Interprétation de la valeur de propriété

L’union de valeur de propriété et les données de valeur doivent être interprétées en fonction de la balise de propriété dans les 4 octets du bloc de propriété. Cette balise de propriété a le même format qu’une balise de propriété MAPI. Les bits 0 à 15 de l’indicateur de propriété correspondent au type de propriété. Les bits 16 à 31 correspondent à l’identificateur de la propriété. Le type de propriété détermine comment le reste de la propriété doit être lu.
  
## <a name="static-value"></a>Valeur statique

Certaines propriétés ne possèdent aucune valeur de données et ont uniquement des données dans l’union. Les types de propriété suivants (qui proviennent de la balise de propriété) doivent interpréter les Union de données de propriété à 8 octets comme suit :
  
|**Type de proposition**|**Interprétation de l’union de propriété**|
|:-----|:-----|
|PT_I2  <br/> |short int  <br/> |
|PT_LONG  <br/> |long  <br/> |
|PT_R4  <br/> |float  <br/> |
|PT_DOUBLE  <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |short int  <br/> |
|PT_SYSTIME  <br/> |FILETIME  <br/> |
|PT_I8  <br/> |LARGE_INTEGER  <br/> |
   
## <a name="dynamic-values"></a>Valeurs dynamiques

Les autres propriétés possèdent des données dans un bloc de données de la valeur après que les 16 premiers octets contiennent la balise de propriété, les données réservées et l’union de valeur de propriété. Contrairement aux valeurs statiques, les données stockées dans l’union de valeur de propriété de 8 octets ne sont pas pertinentes à la lecture. Lorsque vous rédigez, assurez-vous que vous complétez correctement ces 8 octets. Toutefois, le contenu des 8 octets n’est pas important. Dans les valeurs dynamiques, le type de la balise de propriété détermine la manière d’interpréter les données de valeur.
  
PT_STRING8 
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre d’octets n  <br/> |4  <br/> |
|Les octets seront interprétés comme une chaîne ANSI (y compris terminateur NULL)  <br/> |n  <br/> |
   
PT_CLSID
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Les octets seront interprétés comme un GUID  <br/> |Seiz  <br/> |
|||
   
PT_BINARY 
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre d’octets n  <br/> |4  <br/> |
|Les octets seront interprétés comme une gamme d’octets  <br/> |n  <br/> |
   
PT_ERROR
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre d’octets n  <br/> |4  <br/> |
|Les octets seront interprétés comme une gamme d’octets  <br/> |n  <br/> |
   
PT_MV_BINARY
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de matrices binaires X  <br/> |4  <br/> |
|Une exécution d’octets contenant X matrices binaires. Chaque tableau doit être interprété exactement comme l’exécution d’octet PT_BINARY.  <br/> |Variable  <br/> |
   
PT_MV_STRING8 (Outlook 2007, Outlook 2010, et Outlook 2013)
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de chaînes ANSI X  <br/> |4  <br/> |
|Une exécution d’octets contenant X chaînes ANSI. Chaque tableau doit être interprété exactement comme l’exécution d’octets PT_STRING8.  <br/> |Variable  <br/> |
   
PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)
  
|**Données de la valeur**|**Nombre d’octets**|
|:-----|:-----|
|Nombre de chaînes UNICODE X  <br/> |4  <br/> |
|Une exécution d’octets contenant X chaînes UNICODE. Chaque tableau doit être interprété exactement comme l’exécution d’octets PT_UNICODE.  <br/> |Variable  <br/> |
   
## <a name="significant-properties"></a>Propriétés importantes

Comme mentionné précédemment dans cette rubrique, les blocs binaires qui représentent les propriétés possèdent des balises de propriété correspondant aux propriétés destinataires du carnet d’adresses. Pour les propriétés qui ne sont pas répertoriées ici, vous pouvez consulter la description de la propriété àhttps://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.
  
|**Nom de la propriété**|**Balise de propriété**|**Description (pour plus d’informations, consultez MSDN)**|
|:-----|:-----|:-----|
|PR_NICK_NAME_W (non transmis aux destinataires, spécifiques uniquement aux flux de saisie semi-automatique)  <br/> |0x6001001f  <br/> |Cette propriété doit être la première dans chaque ligne du destinataire. Sur le plan opérationnel, elle correspond à un identificateur de clé pour la ligne du destinataire.  <br/> |
|PR_ENTRYID  <br/> |0x0FFF0102  <br/> |L’identificateur d’entrée Carnet d’adresses du destinataire.  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Le nom d’affichage du destinataire.  <br/> |
|PR_EMAIL_ADDRESS_W  <br/> |0x3003001F  <br/> |Adresse de courrier du destinataire (par exemple, johndoe@contoso.com ou /o=Contoso/OU=Foo/cn=Destintaires/cn=Durand)  <br/> |
|PR_ADDRTYPE_W  <br/> |0x3002001F  <br/> |Type d’adresse du destinataire (par exemple, SMTP ou EX).  <br/> |
|PR_SEARCH_KEY  <br/> |0x300B0102  <br/> |Clé de recherche MAPI du destinataire.  <br/> |
|PR_SMTP_ADDRESS_W  <br/> |0x39FE001f  <br/> |Adresse SMTP du destinataire.  <br/> |
|PR_DROPDOWN_DISPLAY_NAME_W (non transmis aux destinataires, spécifiques uniquement aux flux de saisie semi-automatique)  <br/> |0X6003001f  <br/> |La chaîne d’affichage qui s’affiche dans la liste de saisie semi-automatique.  <br/> |
|PR_NICK_NAME_WEIGHT (non transmis aux destinataires, spécifiques uniquement aux flux de saisie semi-automatique)  <br/> |0x60040003  <br/> |La pondération de cette entrée de saisie semi-automatique. La pondération est utilisée pour déterminer dans quel ordre les entrées de saisie semi-automatique se produisent lorsqu’elles correspondent à la liste de saisie semi-automatique. Les entrées ayant une pondération supérieure s’affichent avant les entrées ayant une pondération inférieure. La liste complète de saisie semi-automatique est triée par cette propriété. La pondération diminue régulièrement au fil du temps et augmente lorsque l’utilisateur envoie un message électronique à ce destinataire. Consultez la description plus loin dans cette rubrique pour plus d’informations sur cette propriété.  <br/> |
   
PR_NICK_NAME_WEIGHT
  
L’ensemble de lignes dans le flux de saisie semi-automatique est trié dans l’ordre décroissant par la propriété PR_NICK_NAME_WEIGHT et le flux de saisie semi-automatique doit toujours conserver cette caractéristique triée. Par conséquent, les modifications apportées à la pondération de ligne doivent également assurer que la position de la ligne conserve l’ordre trié de l’ensemble complet de lignes. Les ajouts apportés à l’ensemble de ligne doivent être insérés à l’emplacement correct afin de conserver l’ordre trié.
  
La valeur minimale de cette pondération est 0 x 1 et la valeur maximale est LONG_MAX. Toutes les autres valeurs concernant la pondération sont considérées comme non valides.
  
Lorsqu’Outlook 2007 envoie un courrier ou résout un destinataire, il augmentera la pondération du destinataire par 0 x 2000.
  

