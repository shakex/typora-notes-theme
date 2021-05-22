# Notes Light

A typora theme inspired by [**Apple Notes**](https://support.apple.com/guide/notes/welcome/mac) (light mode🌝), modified from [typora-notes-dark-theme](https://github.com/adesurirey/typora-notes-dark-theme) for personal use preference. 



> **Note**
>
> Typora是一款强大的Markdown格式的文本编辑器， Typora为您提供了作为读者和作家的无缝体验。它删除所有其他不必要的干扰，提供了一个真正的实时预览功能，帮助您专注于内容本身。



## How to install

- [x] **Clone or download the latest release of *typora-notes-theme*.**

  ```bash
  git clone https://github.com/shakex/typora-notes-theme.git
  ```

- [ ] Open typora. click <kbd>Open Theme Folder</kbd> button from `Preference` Panel -> `Appearance` section.

- [ ] Put `notes-light.css` and `notes-light/` folder into the opened folder, make sure your css files are directory under that directory.

- [ ] Restart typora. choose `Notes Light` theme and enjoy. 🤗



## 💡Spotlight

### *Jupyter-look* syntax highlighting

```python
# syntax highlighting inspired from JupyterLab Light theme 
# sample code
class LeNet5(BaseBackbone):
    """`LeNet5 <https://en.wikipedia.org/wiki/LeNet>`_ backbone.

    The input for LeNet-5 is a 32×32 grayscale image.

    Args:
        num_classes (int): number of classes for classification.
            The default value is -1, which uses the backbone as
            a feature extractor without the top classifier.
    """

    def __init__(self, num_classes=-1):
        super(LeNet5, self).__init__()
        self.num_classes = num_classes
        self.features = nn.Sequential(
            nn.Conv2d(1, 6, kernel_size=5, stride=1), nn.Tanh(),
            nn.AvgPool2d(kernel_size=2),
            nn.Conv2d(6, 16, kernel_size=5, stride=1), nn.Tanh(),
            nn.AvgPool2d(kernel_size=2),
            nn.Conv2d(16, 120, kernel_size=5, stride=1), nn.Tanh())
        if self.num_classes > 0:
            self.classifier = nn.Sequential(
                nn.Linear(120, 84),
                nn.Tanh(),
                nn.Linear(84, num_classes),
            )

    def forward(self, x):
        x = self.features(x)
        if self.num_classes > 0:
            x = self.classifier(x.squeeze())
        return x
```

