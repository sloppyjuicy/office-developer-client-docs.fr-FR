---
<<<<<<< Titre tête : convertir les tableaux de Microsoft Access, les formulaires et rapports TOCTitle : convertir Microsoft Access Tables, formulaires et rapports ms:assetid : cc170e62-a663-60e8-4446-07a7a874b747 ms:mtpsurl : https://msdn.microsoft.com/library/Ff834413(v=office.15) ms:contentKeyID : ms.date 48547731 : 18/09/2015 === titre : convertir Microsoft Access tables, formulaires et rapports TOCTitle : convertir Microsoft Access tables, formulaires et rapports description : les modifications introduites par Microsoft Access 2002 risquent d’affecter le comportement de votre version 1. x ou 2.0 applications.
MS:AssetId : cc170e62-a663-60e8-4446-07a7a874b747 ms:mtpsurl : https://msdn.microsoft.com/library/Ff834413(v=office.15) ms:contentKeyID : ms.date 48547731 : 10/16/2018
>>>>>>> maître mtps_version : v=office.15 f1_keywords :
- vbaac10.chm5187104 f1_categories :
- Office.Version=v15
---

<<<<<<< Tête
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Convertir les tables, les formulaires et les états Microsoft Access
=======
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Convertir les tables, formulaires et états Microsoft Access
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

Plusieurs modifications introduites par Microsoft Access 2002 risquent d'affecter le fonctionnement de vos applications des versions 1.*x* et 2.0. Les sections suivantes vous apportent plus d'informations sur ces modifications.

<<<<<<< Tête
## <a name="indexes-and-relationships"></a>Index et relations

Une table Microsoft Access peut contenir jusqu'à 32 index. Des tables très complexes faisant partie de plusieurs relations peuvent parfois dépasser le nombre d'index permis ; vous ne pourrez dès lors pas convertir la base de données qui contient ces tables. Le moteur de base de données Microsoft Access crée des index des deux côtés des relations entre les tables. Si vous ne parvenez pas à convertir votre base de données, supprimez quelques relations et essayez de nouveau.

## <a name="the-limittolist-property-of-combo-boxes"></a>Propriété LimitToList des zones de liste modifiable

Dans Microsoft Access 2002 ou version ultérieure, zones de liste déroulante acceptent les valeurs **Null** lorsque la propriété **LimitToList** est définie sur **True** (– 1), si la liste contienne des valeurs **Null** ou non. Dans la version 2.0, une zone de liste modifiable dont la propriété **LimitToList** a la valeur **True** accepte une valeur **Null** , sauf si la liste contient une valeur **Null** . Si vous souhaitez empêcher les utilisateurs d’entrer une valeur **Null** à l’aide d’une zone de liste déroulante, définissez la propriété **Required** du champ de la table **Oui**.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>Menus et activation d'objets OLE en place

Pour accéder aux fonctionnalités supplémentaires lorsque vous activez des objets OLE en place, il se peut que certaines commandes de menu aient été déplacées vers un menu qui n'est pas remplacé lorsque vous activez un serveur OLE.

Les macros de votre application convertie qui utilisent une action ExécuterElémentMenu pour exécuter une commande de menu de la version 2.0 lors de l'activation d'une application ne seront pas affectées par les modifications. Les commandes de la version 2.0 correspondent à leur équivalent dans les versions ultérieures de Microsoft Access.

## <a name="referencing-a-control-on-a-read-only-form"></a>Référence à un contrôle de formulaire en lecture seule

Dans Microsoft Access 2002 ou une version ultérieure, vous ne pouvez pas utiliser d'expression pour faire référence à la valeur d'un contrôle de formulaire en lecture seule qui lié d'une source d'enregistrement vide. Dans les versions précédentes, l'expression renvoyait la valeur **Null**. Avant de faire référence à un contrôle dans un formulaire en lecture seule, vous devez vérifier que la source d'enregistrement du formulaire contient des enregistrements.

## <a name="date-fields-and-data-entry"></a>Champs Date et saisie de données

Si vous tapez **3/3** dans un champ de type Date d'une feuille de données de formulaire ou de table, Microsoft Access 2002, ou une version ultérieure, y insère automatiquement l'année en cours. Toutefois, si vous tapez **3/3/** dans le même champ, Microsoft Access renvoie un message d'erreur. Vous devez omettre le dernier délimiteur de date, afin que Microsoft Access puisse convertir la date dans le format correct.

## <a name="buttons-created-with-the-command-button-wizard"></a>Boutons créés à l'aide de l'Assistant Bouton de commande

Si vous utilisiez l'Assistant Bouton de commande dans les versions 2.0 et 7.0 de Microsoft Access pour générer du code qui appelait une autre application, vous devez supprimer le bouton et le créer de nouveau à l'aide de l'Assistant Bouton de commande de Microsoft Access 2002 ou version ultérieure.

## <a name="form-and-report-class-modules"></a>Modules de classe de formulaire et d'état

Dans les versions de Microsoft Access antérieures à 2002, les objets de **formulaire** et **d’état** ont des modules de classe associés même si aucun code-behind de l’objet. Dans Microsoft Access 2002 ou version ultérieure, vous pouvez définir un formulaire ou d’état à la propriété **HasModule** sur **False**. Lorsque vous définissez la propriété **HasModule** sur **False**, le formulaire ou l’état occupera moins d’espace disque et se chargera plus rapidement, car il n’a plus un module de classe associé.

## <a name="converted-version-20-report-has-different-margins"></a>Un état converti à partir de la version 2.0 comporte des marges différentes
=======
## <a name="indexes-and-relationships"></a>Index et relations

Une table Microsoft Access peut contenir jusqu'à 32 index. Des tables très complexes faisant partie de plusieurs relations peuvent parfois dépasser le nombre d'index permis ; vous ne pourrez dès lors pas convertir la base de données qui contient ces tables. Le moteur de base de données Microsoft Access crée des index des deux côtés des relations entre les tables. Si vous ne parvenez pas à convertir votre base de données, supprimez quelques relations et essayez de nouveau.

## <a name="the-limittolist-property-of-combo-boxes"></a>Propriété LimitToList des zones de liste déroulante

Dans Microsoft Access 2002 ou version ultérieure, zones de liste déroulante acceptent les valeurs **Null** lorsque la propriété **LimitToList** est définie sur **True** (– 1), si la liste contienne des valeurs **Null** ou non. Dans la version 2.0, une zone de liste modifiable dont la propriété **LimitToList** a la valeur **True** accepte une valeur **Null** , sauf si la liste contient une valeur **Null** . Si vous souhaitez empêcher les utilisateurs d’entrer une valeur **Null** à l’aide d’une zone de liste déroulante, définissez la propriété **Required** du champ de la table **Oui**.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>Menus et activation sur place des objets OLE

Pour accéder aux fonctionnalités supplémentaires disponibles pour vous lors de l’activation des objets OLE en place, certaines commandes de menu peuvent ont été déplacés vers un menu qui n’est pas remplacé lorsque vous activez un serveur OLE.

Les macros de votre application convertie qui utilisent une action ExécuterElémentMenu pour exécuter une commande de menu de la version 2.0 lors de l'activation d'une application ne seront pas affectées par les modifications. Les commandes de la version 2.0 correspondent à leur équivalent dans les versions ultérieures de Microsoft Access.

## <a name="referencing-a-control-on-a-read-only-form"></a>Référence à un contrôle sur un formulaire en lecture seule

Dans Microsoft Access 2002 ou une version ultérieure, vous ne pouvez pas utiliser d'expression pour faire référence à la valeur d'un contrôle de formulaire en lecture seule qui lié d'une source d'enregistrement vide. Dans les versions précédentes, l'expression renvoyait la valeur **Null**. Avant de faire référence à un contrôle dans un formulaire en lecture seule, vous devez vérifier que la source d'enregistrement du formulaire contient des enregistrements.

## <a name="date-fields-and-data-entry"></a>Champs date et saisie de données

Si vous tapez **3/3** dans un champ de type Date d'une feuille de données de formulaire ou de table, Microsoft Access 2002, ou une version ultérieure, y insère automatiquement l'année en cours. Toutefois, si vous tapez **3/3/** dans le même champ, Microsoft Access renvoie un message d'erreur. Vous devez omettre le dernier délimiteur de date, afin que Microsoft Access puisse convertir la date dans le format correct.

## <a name="buttons-created-with-the-command-button-wizard"></a>Boutons créés avec l’Assistant bouton de commande

Si vous utilisiez l'Assistant Bouton de commande dans les versions 2.0 et 7.0 de Microsoft Access pour générer du code qui appelait une autre application, vous devez supprimer le bouton et le créer de nouveau à l'aide de l'Assistant Bouton de commande de Microsoft Access 2002 ou version ultérieure.

## <a name="form-and-report-class-modules"></a>Modules de classe de formulaire et d’état

Dans les versions de Microsoft Access antérieures à 2002, les objets de **formulaire** et **d’état** ont des modules de classe associés même si aucun code-behind de l’objet. Dans Microsoft Access 2002 ou version ultérieure, vous pouvez définir un formulaire ou d’état à la propriété **HasModule** sur **False**. Lorsque vous définissez la propriété **HasModule** sur **False**, le formulaire ou l’état occupera moins d’espace disque et se chargera plus rapidement, car il n’a plus un module de classe associé.

## <a name="converted-version-20-report-has-different-margins"></a>Un état converti version 2.0 comporte des marges différentes
>>>>>>> master

Vous rencontrerez peut-être des problèmes lors de l'impression ou de l'affichage en mode Aperçu avant impression d'un état dans Microsoft Access 2002 ou version ultérieure qui a été converti à partir de Microsoft Access 2.0 si certaines de ses marges ont pour valeur 0. Lorsque vous convertissez un état Microsoft Access 2.0, les marges n'ont pas pour valeur 0 ; elles se voient attribuer la valeur minimale de marge valide pour l'imprimante par défaut. Cela empêche ainsi l'état d'imprimer des données dans la zone non imprimable de l'imprimante.

Pour résoudre ce problème, réduisez la largeur des colonnes, l'espace entre les colonnes et le nombre de colonnes dans l'état, de sorte que la largeur des colonnes ajoutée à la largeur des marges par défaut soit égale ou inférieure à la largeur de votre papier.

<<<<<<< Tête
## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>Impossible d'utiliser la propriété Format pour distinguer les valeurs Null des chaînes vides

Dans les versions 1. *x* et 2.0, vous pouvez utiliser la propriété **Format** d’un contrôle pour afficher des valeurs différentes pour les valeurs **Null** des chaînes de longueur nulle ( » «). Dans Microsoft Access 2002 ou version ultérieure, pour distinguer les valeurs de type **Null** des chaînes vides dans un contrôle de formulaire, paramétrez la propriété **ControlSource** d'un contrôle sur une expression qui teste la présence de valeurs **Null**. Par exemple, pour afficher « Null » ou « ZLS » dans un contrôle, paramétrez sa propriété **ControlSource** sur l'expression suivante :

<a name="iifisnullmycontrol-null-formatmycontrol-zls"></a>\=IIf (IsNull (\[mon\]), « Null », Format (\[mon\], « @; ;ZLS")) »))
=======
## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>Impossible d’utiliser la propriété Format pour distinguer les valeurs Null des chaînes de longueur nulle

Dans les versions 1. *x* et 2.0, vous pouvez utiliser la propriété **Format** d’un contrôle pour afficher des valeurs différentes pour les valeurs **Null** des chaînes de longueur nulle ( » «). Dans Microsoft Access 2002 ou version ultérieure, pour distinguer les valeurs de type **Null** des chaînes vides dans un contrôle de formulaire, paramétrez la propriété **ControlSource** d'un contrôle sur une expression qui teste la présence de valeurs **Null**. Par exemple, pour afficher « Null » ou « ZLS » dans un contrôle, paramétrez sa propriété **ControlSource** sur l'expression suivante :

`=IIf(IsNull([MyControl]), "Null", Format([MyControl], "@;ZLS"))`
>>>>>>> master

