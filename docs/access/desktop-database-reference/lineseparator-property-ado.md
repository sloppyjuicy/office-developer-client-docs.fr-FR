---
<<<<<<< Titre tête : LineSeparator propriété (ADO) TOCTitle : LineSeparator propriété (ADO) === titre : LineSeparator, propriété (ADO) TOCTitle : LineSeparator, propriété (ADO)
>>>>>>> Master ms:assetid : 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID : ms.date 48546676 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="lineseparator-property-ado"></a>LineSeparator, propriété (ADO)
=======
# <a name="lineseparator-property-ado"></a>LineSeparator, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le caractère binaire à utiliser comme le séparateur de ligne dans des objets [Stream](stream-object-ado.md) textuels.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur [LineSeparatorsEnum](lineseparatorsenum.md) qui indique le caractère séparateur de ligne utilisé dans le **Stream**. La valeur par défaut est **adCRLF**.

## <a name="remarks"></a>Remarques

**LineSeparator** sert à interpréter les lignes à la lecture du contenu d'un **Stream** textuel. Les lignes peuvent être ignorées grâce à la méthode [SkipLine](skipline-method-ado.md).

**LineSeparator** n’est utilisé qu’avec les objets **Stream** textuels (dont le [Type](type-property-ado-stream.md) est **adTypeText**). Cette propriété est ignorée si le **Type** est **adTypeBinary**.

