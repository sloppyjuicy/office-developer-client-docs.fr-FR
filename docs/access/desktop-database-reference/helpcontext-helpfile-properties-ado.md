---
<<<<<<< Titre tête : HelpContext, HelpFile propriétés (ADO) TOCTitle : HelpContext, HelpFile propriétés (ADO) ms:assetid : 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl : https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID : ms.date 48546194 : 09/18 / 2015 mtps_version : v=office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext, HelpFile, propriétés (ADO)

=== titre : HelpContext, HelpFile, propriétés (ADO) TOCTitle : HelpContext, HelpFile propriétés (ADO) ms:assetid : 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl : https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID : ms.date 48546194 : 17/10/2018 mtps_version : v=office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext, HelpFile, propriétés (ADO)
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

Indique le fichier d'aide et la rubrique associés à un objet [Error](error-object-ado.md).

<<<<<<< Tête
## <a name="return-values"></a>Valeurs renvoyées

  - **HelpContextID**: renvoie un ID de contexte pour une rubrique de fichier d'aide sous forme de valeur **Long**.

  - **HelpFile**: renvoie une valeur **String** qui correspond à un chemin d'accès à un fichier d'aide entièrement résolu.
=======
## <a name="return-values"></a>Valeurs de retour

- **HelpContextID**: renvoie un ID de contexte pour une rubrique de fichier d'aide sous forme de valeur **Long**.

- **HelpFile**: renvoie une valeur **String** qui correspond à un chemin d'accès à un fichier d'aide entièrement résolu.
>>>>>>> master

## <a name="remarks"></a>Remarques

Si un fichier d'aide est spécifié dans la propriété **HelpFile**, la propriété **HelpContext** permet d'afficher automatiquement la rubrique d'aide qu'elle identifie. Si aucune rubrique d'aide pertinente n'est disponible, la propriété **HelpContext** renvoie zéro et la propriété **HelpFile** renvoie une chaîne vide (« »).

