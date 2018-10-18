---
<<<<<<< Titre tête : TOCTitle Position propriété (ADO) : Position propriété (ADO) === titre : Position, propriété (ADO) TOCTitle : Position, propriété (ADO)
>>>>>>> Master ms:assetid : a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID : ms.date 48546709 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="position-property-ado"></a>Position, propriété (ADO)
=======
# <a name="position-property-ado"></a>Position, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique la position actuelle dans un objet [Stream](stream-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou retourne une valeur de type **Long** qui spécifie le décalage, en nombre d'octets, de la position actuelle par rapport au début du flux. La valeur par défaut est 0 ; elle représente le premier octet du flux.

## <a name="remarks"></a>Remarques

La position actuelle peut être définie au-delà de la fin du flux. Dans ce cas, la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** est augmentée en conséquence. Les nouveaux octets ajoutés de cette façon sont nuls.


> [!NOTE]
> <P>[!REMARQUE] <STRONG>Position</STRONG> mesure toujours des octets. Pour les flux de texte utilisant des jeux de caractères multioctet, multipliez la position par la taille de caractères pour déterminer le numéro du caractère. Par exemple, dans un jeu de caractères de deux octets, le premier caractère est en position 0, le deuxième en position 2, le troisième en position 4, etc.</P>



Il est impossible d'utiliser des valeurs négatives pour modifier la position actuelle dans un **Stream**. La propriété **Position** n'accepte que les chiffres positifs.

Pour les objets **Stream** en lecture seule, ADO ne renvoie pas une erreur si la **Position** est définie sur une valeur supérieure à la **taille** du **flux de données**. Cela ne pas modifier la taille du **flux**ou **son contenu** . Toutefois, cette opération doit être évitée, car elle génère une valeur de **Position** sans signification.

