---
components:
    - rx.data_list.root
---

```python exec
import reflex as rx
```

# Data List

The `DataList` component displays key-value pairs and is particularly helpful for showing metadata.

A `DataList` needs to be initialized using `rx.data_list.root()` and currently takes in data list items: `rx.data_list.item`

```python demo
rx.card(
                rx.data_list.root(
                    rx.data_list.item(
                        rx.data_list.label("Status"),
                        rx.data_list.value(
                            rx.badge(
                                "Authorized",
                                variant="soft",
                                radius="full",
                            )
                        ),
                        align="center",
                    ),
                    rx.data_list.item(
                        rx.data_list.label("ID"),
                        rx.data_list.value(rx.code("U-474747")),
                    ),
                    rx.data_list.item(
                        rx.data_list.label("Name"),
                        rx.data_list.value("Developer Success"),
                        align="center",
                    ),
                    rx.data_list.item(
                        rx.data_list.label("Email"),
                        rx.data_list.value(
                            rx.link(
                                "success@reflex.dev",
                                href="mailto:success@reflex.dev",
                            ),
                        ),
                    ),
                    rx.data_list.item(
                        rx.data_list.label("Company"),
                        rx.data_list.value(
                            rx.link(
                                "Reflex",
                                href="https://reflex.dev",
                            ),
                        ),
                    ),
                ),
            ),
```